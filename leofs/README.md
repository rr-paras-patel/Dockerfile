# Docker-LeoFS
Docker container images for LeoFS all in one node(Manager_Master, Manager_Slave, Storage, Gateway).
### Installation
```
$ docker pull paraspatel/leofs:latest
OR
$ docker pull paraspatel/leofs:1.2.21
```
### Build
Periodically we will push all stable verion of leofs based on CentoOS v6.6. but if you want to build your own customize images run bellow build command from your `Dockerfile` Directory
```
docker build -t leofs:1.2.21 .
```
### Start LeoFS
Expose and forward port based on your requirement basically we  target `SSH:22`, `Manager:10010` adn `Gateway:8080`. if we want to access it outside container you may also link application container to acess it privately.
```
$ docker run -itd  -p 8080:8080 -p 10010:10010 leofs:1.2.21
```
### Confirm container ID
```
$ docker ps -a -q
{Container ID}
```
### Check boot log of container
```
$ docker logs {Container ID}
* Starting OpenBSD Secure Shell server sshd
Generating RING...
Generated RING
OK 100% - storage_0@127.0.0.1
OK
LeoFS is ready!!
```

### Confirm IP Address and port
```
$ docker inspect {Container ID} | grep 'Port\|IPAddress'
"PortBindings": {
                        "HostPort": "10010"
                        "HostPort": "8080"
            "PublishAllPorts": false,
    "IPAddress": "172.17.0.XXX",
```

### Get into your container
```
docker exec -i -t {Container ID} bash
$ leofs-adm status
[System Confiuration]
-----------------------------------+----------
Item                              | Value    
-----------------------------------+----------
Basic/Consistency level
-----------------------------------+----------
                   system version | 1.2.21
                       cluster Id | leofs_1
                            DC Id | dc_1
                   Total replicas | 1
         number of successes of R | 1
         number of successes of W | 1
         number of successes of D | 1
number of rack-awareness replicas | 0
                        ring size | 2^128
-----------------------------------+----------
Multi DC replication settings
-----------------------------------+----------
       max number of joinable DCs | 2
          number of replicas a DC | 1
-----------------------------------+----------
Manager RING hash
-----------------------------------+----------
                current ring-hash | 433fe365
               previous ring-hash | 433fe365
-----------------------------------+----------

[State of Node(s)]
-------+--------------------------+--------------+----------------+----------------+----------------------------
type  |           node           |    state     |  current ring  |   prev ring    |          updated at         
-------+--------------------------+--------------+----------------+----------------+----------------------------
 S    | storage_0@127.0.0.1      | running      | 433fe365       | 433fe365       | 2016-04-25 04:44:39 +0000
 G    | gateway_0@127.0.0.1      | running      | 433fe365       | 433fe365       | 2016-04-25 04:44:45 +0000
-------+--------------------------+--------------+----------------+----------------+----------------------------
```
