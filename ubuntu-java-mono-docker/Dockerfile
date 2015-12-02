# docker run -e TEAMCITY_SERVER=http://buildserver:8111 -dt -p 9090:9090 ariya/centos7-teamcity-agent

FROM monster/ubuntu-java-mono
MAINTAINER Ahmed Hassanien <ahmed_hassanien@otasys.com>

RUN sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D && \
	sudo echo "deb http://apt.dockerproject.org/repo ubuntu-trusty main" > /etc/apt/sources.list.d/docker.list && \
	sudo apt-get -q update && \
	sudo apt-get -yq install docker-engine && \
        sudo apt-get -y autoremove && \
        sudo apt-get clean && \
        sudo rm -rf /var/lib/apt/lists/* /var/tmp/*

