# Docker
[![Circle CI](https://circleci.com/gh/PatelParas/Dockerfile/tree/master.svg?style=svg)](https://circleci.com/gh/PatelParas/Dockerfile/tree/master)
A repository contains Dockerfiles for various purpose and information to build and run those docker images

## Container Technologies Memo for Personal Use
### Private Registry
- [Docker Trusted Registry](https://www.docker.com/products/docker-trusted-registry)(Full Matured and PROD ready)
- [GitLab Registry](https://about.gitlab.com/downloads/#centos6)
- [Quay.io](https://quay.io/) (Docker, App Container)
- [Google Container Registry](https://cloud.google.com/tools/container-registry/) (Docker)
- [Reesd](https://reesd.com/) (Docker)
- [Amazon EC2 Container Registry](https://aws.amazon.com/ecr/)
- [CoreOS Enterprise Registry](https://coreos.com/products/enterprise-registry/)
- [Detail Pros and Cons Listed here](http://www.slant.co/topics/2436/viewpoints/6/~docker-image-private-registries~coreos-enterprise-registry)

### Docker Image Analysis tools
- [Imagelayers.io by CenturyLink](https://imagelayers.io/)

### A curated list of awesome container technologies inspired by awesomes.

- [runc](https://github.com/opencontainers/runc)
- [jetpack](https://github.com/3ofcoins/jetpack)
- [nosecone](https://github.com/cdaylward/nosecone)
- [rkt](https://github.com/coreos/rkt) 
- [Docker](https://www.docker.com/) 
- [systemd-nspawn](http://fedoraproject.org/wiki/Features/SystemdLightweightContainers)
- [lmctfy](https://github.com/google/lmctfy)
- [garden](https://github.com/cloudfoundry-incubator/garden)
- [warden](https://github.com/cloudfoundry/warden)
- [LXC](https://linuxcontainers.org/)
- [OpenVZ](https://openvz.org/Main_Page)
- [Solaris Zones](http://docs.oracle.com/cd/E26502_01/html/E29024/toc.html)
- [FreeBSD jail](http://www.freebsd.org/cgi/man.cgi?query=jail&format=html)
- [zerovm](https://github.com/zerovm/zerovm)
- [mbox](https://github.com/tsgates/mbox)
- [vagga](https://github.com/tailhook/vagga)
- [MINCS](https://github.com/mhiramat/mincs)
- [Linux-VServer](http://linux-vserver.org/)
- [pflask](https://github.com/ghedo/pflask)
- [cask](https://github.com/ianpreston/cask)
- [shocker](https://github.com/stamf/shocker)
- [firejail](https://github.com/netblue30/firejail)


### Spec

- [opencontainers/specs](https://github.com/opencontainers/specs)
- [appc/spec](https://github.com/appc/spec)

### OS 

Light-weight (Minimal) OS for running containers.

- [boot2docker](http://boot2docker.io/) 
- [CoreOS](https://coreos.com/) from CoreOS
- [Project Atomic](http://www.projectatomic.io/) from Red Hat
- [Snappy Ubuntu Core](http://www.ubuntu.com/cloud/tools/snappy) from Canonical
- [RancherOS](http://rancher.com/rancher-os/) from Rancher Labs
- [Photon](https://vmware.github.io/photon/) from VMware
- [Nano Server]([http://blogs.technet.com/b/windowsserver/archive/2015/04/08/microsoft-announces-nano-server-for-modern-apps-and-cloud.aspx) from Windows

### Cluster Management

- [kubernetes](http://kubernetes.io/)
- [Tectonic](https://tectonic.com/)
- [lattice](http://lattice.cf/index.html)
- [Panamax](http://panamax.io/)
- [Flocker](https://github.com/ClusterHQ/flocker)
- [VirtKick](https://github.com/virtkick)

### Networking

* [wormhole](https://github.com/vishvananda/wormhole)
* [Calico-Docker](https://www.projectcalico.org/getting-started/docker/) - Calico is a pure layer 3 virtual network that allows containers over multiple docker-hosts to talk to each other.
* [Flannel](https://github.com/coreos/flannel/) - Flannel is a virtual network that gives a subnet to each host for use with container runtimes.
* [Wagl](https://github.com/ahmetalpbalkan/wagl) - DNS Service Discovery for Docker Swarm (by [@ahmetalpbalkan][ahmetalpbalkan] ) http://ahmetalpbalkan.github.io/wagl/
* [Weave][weave] (The Docker network) - Weave creates a virtual network that connects Docker containers deployed across multiple hosts.


## Logging
* [Docker-Fluentd][fluentd] - Docker container to Log Other Containers' Logs. One can aggregate the logs of Docker containers running on the same host using Fluentd by [@kiyoto][kiyoto]
* [LogJam](https://github.com/gocardless/logjam) - Logjam is a log forwarder designed to listen on a local port, receive log entries over UDP, and forward these messages on to a log collection server (such as logstash) by [@gocardless](https://github.com/gocardless)
* [Logspout](https://github.com/gliderlabs/logspout) - Log routing for Docker container logs by [@gliderlabs][gliderlabs]
* [Logsene for Docker][spm] Monitoring of Metrics, Events and Logs implemented in Node.js. Integrated [logagent-js](https://github.com/sematext/logagent-js) to detect and parse various log formats. [@sematext][sematext]
* [Out-of-the-box Host/Container Monitoring/Logging/Alerting Stack](https://github.com/uschtwill/docker_monitoring_logging_alerting) Docker host and container monitoring, logging and alerting out of the box using cAdvisor, Prometheus, Grafana for monitoring, Elasticsearch, Kibana and Logstash for logging and elastalert and Alertmanager for alerting. Set up in 5 Minutes. Secure mode for production use with built-in [Automated Nginx Reverse Proxy (jwilder's)][nginxproxy].


### Monitoring

- [cAdvisor](https://github.com/google/cadvisor)

### PaaS 

- [Flynn](https://flynn.io/) (Docker)
- [Deis](http://deis.io/) (Docker)
- [dokku](https://github.com/progrium/dokku) (Docker)
- [Cloud Foundry](http://cloudfoundry.org/index.html) (Warden)
- [OpenShift v3](https://github.com/openshift/origin) (Docker, Kubernetes)

## Service

### Hosting

- [Google Container Engine](https://cloud.google.com/container-engine/)
- [Google App Engine Managed VM](https://cloud.google.com/appengine/docs/managed-vms/)
- [Amazon EC2 Container Service](http://aws.amazon.com/ecs/)
- [Amazon Elastic Beanstalk](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_docker.html)
- [Triton](https://www.joyent.com/)
- [tutum](https://www.tutum.co/)
- [StackDock](https://stackdock.com/)
- [Giant Swarm](https://giantswarm.io/)

## Reverse Proxy
* [docker-proxy](https://github.com/silarsis/docker-proxy) - Transparent proxy for docker containers, run in a docker container. By [@silarsis](https://github.com/silarsis)
* [fabio](https://github.com/eBay/fabio) - A fast, modern, zero-conf load balancing HTTP(S) router for deploying microservices managed by consul. By [@eBay](https://github.com/eBay)
* [h2o-proxy](https://github.com/zchee/h2o-proxy) - Automated H2O reverse proxy for Docker containers. An alternative to [jwilder/nginx-proxy][nginxproxy] by [@zchee](https://github.com/zchee)
* [Let's Encrypt Nginx-proxy Companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion) - A lightweight companion container for the nginx-proxy. It allow the creation/renewal of Let's Encrypt certificates automatically. By [@JrCs](https://github.com/JrCs)
* [muguet](https://github.com/mattallty/muguet) - DNS Server & Reverse proxy for Docker environments. By [@mattallty](https://github.com/mattallty)
* [nginx-proxy][nginxproxy] - Automated nginx proxy for Docker containers using docker-gen by [@jwilder][jwilder]
* [Swarm Ingress Router](https://github.com/tpbowden/swarm-ingress-router) - Route DNS names to Swarm services based on labels.
* [Træfɪk](https://traefik.io/) - Automated reverse proxy and load-balancer for Docker, Mesos, Consul, Etcd... By [@EmileVauge](https://github.com/emilevauge)

## Web Interface
* [Docker Registry Browser](https://github.com/klausmeyer/docker-registry-browser) - Web Interface for the Docker Registry HTTP API v2 by [@klausmeyer](https://github.com/klausmeyer)
* [Docker Registry UI](https://github.com/atc-/docker-registry-ui) - A web UI for easy private/local Docker Registry integration by [@atc-](https://github.com/atc-)
* [docker-registry-web](https://github.com/mkuchin/docker-registry-web) - Web UI, authentication service and event recorder for private docker registry v2 by [@mkuchin](https://github.com/mkuchin)
* [docker-swarm-visualizer](https://github.com/manomarks/docker-swarm-visualizer) - Visualizes Docker services on a Docker Swarm (for running demos).
* [dockering-on-rails](https://github.com/Electrofenster/dockerding-on-rails) - Simple Web-Interface for Docker with a lot of features by [@Electrofenster](https://github.com/Electrofenster/)
* [DockerUI](https://github.com/kevana/ui-for-docker) - DockerUI is a web interface to interact with the Remote API by [@crosbymichael][crosbymichael]
* [Portus](https://github.com/SUSE/Portus) - Authorization service and frontend for Docker registry (v2) by [@SUSE](https://github.com/SUSE)
* [Rapid Dashboard](https://github.com/ozlerhakan/rapid) - A simple query dashboard to use Docker Remote API by [@ozlerhakan](https://github.com/ozlerhakan/)

## Local Container Manager
* [Ansible - manage docker containers](http://docs.ansible.com/ansible/docker_module.html)
* [Azk](http://www.azk.io/) - Orchestrate development enviornments on your local machine by [@azukiapp](https://github.com/azukiapp)
* [Beluga](https://github.com/cortexmedia/Beluga) - CLI to deploy docker containers on a single server or low amount of servers. By [@cortextmedia](https://github.com/cortexmedia)
* [Boot2Docker](https://github.com/boot2docker/boot2docker) - Docker for OSX and Windows -- http://boot2docker.io/
* [Dinghy](https://github.com/codekitchen/dinghy) - An alternative way to use Docker on Mac OS X using Docker Machine with virtualbox, vmware, xhyve or parallels
* [DLite](https://github.com/nlf/dlite) - Simplest way to use Docker on OSX, no VM needed. By [@nlf](https://github.com/nlf)
* [docker-vm](https://github.com/shyiko/docker-vm) - Simple and transparent alternative to boot2docker (backed by Vagrant) by [@shyiko](https://github.com/shyiko)
* [Dokku][dokku] - Docker powered mini-Heroku in around 100 lines of Bash by [@progrium][progrium]
* [Dray](https://github.com/CenturyLinkLabs/dray) - An engine for managing the execution of container-based workflows. http://Dray.it by [@CenturyLinkLabs][CenturyLinkLabs]
* [Dusty](http://dusty.gc.com/) - Managed Docker development environments on OS X
* [FuGu](https://github.com/mattes/fugu) - Docker run wrapper without orchestration by [@mattes](https://github.com/mattes)
* [libcompose](https://github.com/docker/libcompose) - Go library for Docker Compose.
* [OctoHost](http://octohost.io/) - Simple web focused Docker based mini-PaaS server. git push to deploy your websites as needed) by [@octohost](https://github.com/octohost)
* [percheron][percheron] - Organise your Docker containers with muscle and intelligence by [@ashmckenzie](https://github.com/ashmckenzie)
* [Shutit](http://ianmiell.github.io/shutit/) - Tool for building and maintaining complex Docker deployments by [@ianmiell][ianmiell]
* [subuser](http://subuser.org) - Makes it easy to securely and portably run graphical desktop applications in Docker
* [Turbo](https://ramitsurana.github.io/turbo/) - Simple and Powerful utility for docker. By [@ramitsurana][ramitsurana]
* [Vagrant - Docker provider](https://www.vagrantup.com/docs/docker/basics.html) - Good starting point is [vagrant-docker-example](https://github.com/bubenkoff/vagrant-docker-example) by [@bubenkoff](https://github.com/bubenkoff)
* [Vessel](https://github.com/awvessel/vessel) - Automates the setup & use of dockerized development environments by [@awvessel](https://github.com/awvessel)

* [Docker Registry v2][distribution] - The Docker toolset to pack, ship, store, and deliver content
* [Rescoyl](https://github.com/noteed/rescoyl) - Private Docker registry by [@noteed][noteed]
* [VMWare Harbor](http://vmware.github.io/harbor/) Project Harbor by VMWare is an enterprise-class registry server that stores and distributes Docker images. Harbor extends the open source Docker Distribution by adding the functionalities usually required by an enterprise, such as security, identity and management.

## Monitoring
* [AppDynamics](https://www.appdynamics.com/community/exchange/extension/docker-monitoring-extension/) - AppDynamics gives enterprises real-time insights into application performance, user performance, and business performance so they can move faster in an increasingly sophisticated, software-driven world.
* [Axibase Time-Series Database](http://axibase.com/products/axibase-time-series-database/writing-data/docker-cadvisor/) - Long-term retention of container statistics and built-in dashboards for Docker. Collected with native Google cAdvisor storage driver.
* [cAdvisor](https://github.com/google/cadvisor) - Analyzes resource usage and performance characteristics of running containers. Created by [@Google](https://github.com/google)
* [Collecting docker logs and stats with Splunk](http://blogs.splunk.com/2015/08/24/collecting-docker-logs-and-stats-with-splunk/)
* [CoScale](http://www.coscale.com/docker-monitoring) - Full stack monitoring for containerized applications and microservices. Powered by anomaly detection to find performance problems faster.
* [Datadog](https://www.datadoghq.com/) - Datadog is a full-stack monitoring service for large-scale cloud environments that aggregates metrics/events from servers, databases, and applications. It includes support for Docker, Kubernetes, and Mesos.
* [Docker-mon](https://github.com/icecrime/docker-mon) - Console-based Docker monitoring by [@icecrime](https://github.com/icecrime)
* [Dockerana](https://github.com/dockerana/dockerana) - packaged version of Graphite and Grafana, specifically targeted at metrics from Docker.
* [DoMonit](https://github.com/eon01/DoMonit) - A simple Docker Monitoring wrapper For Docker API
* [Dynatrace](https://www.dynatrace.com/technologies/cloud-and-microservices/docker-monitoring/) - Monitor containerized applications without installing agents or modifying your Run commands
* [Glances](https://nicolargo.github.io/glances/) - A cross-platform curses-based system monitoring tool written in Python by [@nicolargo](https://github.com/nicolargo)
* [Grafana Docker Dashboard Template](https://grafana.net/dashboards/179) - A template for your Docker, Grafana and Prometheus stack [@vegasbrianc][vegasbrianc]
* [InfluxDB, cAdvisor, Grafana](https://github.com/vegasbrianc/docker-monitoring) - InfluxDB Time series DB in combination with Grafana and cAdvisor by [@vegasbrianc][vegasbrianc]
* [Meros](https://meros.io) - Analyzes containers resources, captures logs, remote web SSH terminal and powerful DevOps alerts.
* [New Relic](https://newrelic.com/partner/docker) - New Relics Docker Monitoring tool
* [Prometheus](https://prometheus.io/) - Open-source service monitoring system and time series database
* [Seagull](https://github.com/tobegit3hub/seagull) - Friendly Web UI to monitor docker daemon. by [@tobegit3hub](https://github.com/tobegit3hub)
* [Site24x7](https://www.site24x7.com/docker-monitoring.html) - Docker MOnitoring for DevOps and IT is a SaaS Pay per Host model
* [SPM for Docker][spm] - Monitoring of host and container metrics, Docker events and logs. Automatic log parser. Anomaly Detection and alerting for metrics and logs. [@sematext][sematext]
* [Sysdig](http://www.sysdig.org/) - An open source troubleshooting tool that provides a rich set of real-time, system-level information. It has container-specific features and is very useful in Docker environments.
* [Zabbix Docker module](https://github.com/monitoringartist/Zabbix-Docker-Monitoring) - Zabbix module that provides discovery of running containers, CPU/memory/blk IO/net container metrics. Systemd Docker and LXC execution driver is also supported. It's a dynamically linked shared object library, so its performance is (~10x) better, than any script solution.
* [Zabbix Docker](https://github.com/gomex/docker-zabbix) - Monitor containers automatically using zabbix LLD feature.

