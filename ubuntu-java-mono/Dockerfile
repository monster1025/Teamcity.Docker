# docker run -e TEAMCITY_SERVER=http://buildserver:8111 -dt -p 9090:9090 ariya/centos7-teamcity-agent

FROM otasys/java:1.8.0_66
MAINTAINER Ahmed Hassanien <ahmed_hassanien@otasys.com>

RUN sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF && \
	echo "deb http://download.mono-project.com/repo/debian wheezy main" | sudo tee /etc/apt/sources.list.d/mono-xamarin.list && \
	sudo apt-get -q update && \
	sudo apt-get -yq install mono-complete && \
	sudo apt-get -y autoremove && \
	sudo apt-get clean && \
	sudo rm -rf /var/lib/apt/lists/* /var/tmp/*
