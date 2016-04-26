FROM ubuntu:14.04
MAINTAINER Paras Patel <parasprince2001@gmail.com>
RUN	apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0AB215679C571D1C8325275B9BDB3D89CE49EC21 \
	&& echo "deb http://ppa.launchpad.net/mozillateam/firefox-next/ubuntu wily main" >> /etc/apt/sources.list.d/firefox.list \

RUN apt-get update && apt-get install -y firefox \
    ca-certificates \
    hicolor-icon-theme \
    libasound2 \
    libgl1-mesa-dri \
    libgl1-mesa-glx \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

RUN export uid=0 gid=0 && \
    mkdir -p /home/developer && \
    echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
    echo "developer:x:${uid}:" >> /etc/group && \
    echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
    chmod 0440 /etc/sudoers.d/developer && \
    chown ${uid}:${gid} -R /home/developer
RUN apt-get install -y firefox \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

USER developer
ENV HOME /home/developer
CMD /bin/bash
ENV LANG="en-US.UTF-8"
COPY local.conf /etc/fonts/local.conf
ENTRYPOINT ["/usr/bin/firefox"]
