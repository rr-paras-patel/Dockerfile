# Docker-Firefox
This is my gentle effort to run GUI based app on container for personal Broswer test Automation.
### Install dependencies
Note: I have started this experiments with Docker-beta on Mac-OS i never tested boot2docker or docker-machine with virtualbox but it should be work with little change your contribution will be appreciated.
```
brew install caskroom/cask/cask-brew
brew cask install xquartz
brew install socat
```
### Expose local xquartz socket
via socat on TCP port 6000 wich give platform to run GUI app on Mac-OS
```
socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"
```
Keep running this in background terminal and use another window
### Find Bridge inet address
Check your bridge inet address we will use it to run application
```
ifconfig bridge100 | grep inet
	inet 192.168.64.1 netmask 0xffffff00 broadcast 192.168.64.255
```
### Run Container
Now all you have to do is pass the DISPLAY address to container in my case as below modify it according to your environment
```
docker run -it --rm -e DISPLAY=192.168.64.1:0 -v /tmp/.X11-unix:/tmp/.X11-unix  paraspatel/firefox:latest
```
### Future work
- Cover all maximum flavors of CentOS and Ubuntu with combination firefox and chrome legacy versions
- Create Linux compatibility for boot2docker  
- Create VNC support with dokcer-machine to support windows, linux and Mac-OS synergy
- Initial idea to make BrowserStack like automated browser rendering test
- Develop Automated capturing(Image) and recording(video) facility
- GUI based automation tool which can run on minimum infrastructure and dependencies
