For Mac OS you need :
Step -->1 : 
```
$brew install socat
```
Step -->2 : 
```
$socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"
```
Step -->3 : Open new command line and run 
```
$docker run -ti --rm -e DISPLAY=192.168.33.1:0 -v /tmp/.X11-unix:/tmp/.X11-unix firefox
```
NOTE:you need to replace IP address with your vboxnet0 Don't run Xquartz manually
