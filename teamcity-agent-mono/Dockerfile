# docker run -e TEAMCITY_SERVER=http://buildserver:8111 -dt -p 9090:9090 ariya/centos7-teamcity-agent

FROM monster/ubuntu-java-mono
MAINTAINER Ahmed Hassanien <ahmed_hassanien@otasys.com>

ADD setupAgent.sh /opt/setupAgent.sh
ADD docker.list /etc/apt/sources.list.d/docker.list

RUN DEBIAN_FRONTEND=noninteractive && \
	chmod +x /opt/setupAgent.sh && \
	apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D && \
	apt-get -q update && \
	apt-get -yq install unzip git && \
	apt-get -yq install docker-engine && \
	apt-get autoremove && \
	rm /bin/sh && ln -s /bin/bash /bin/sh && \
    	apt-get clean && \
    	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/cache/unzip

# Default command.
CMD ["bash", "/opt/setupAgent.sh"]
