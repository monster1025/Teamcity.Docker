FROM otasys/java:1.8.0_66
MAINTAINER Ahmed Hassanien <ahmed_hassanien@otasys.com>

# Environment Variables
ENV TEAMCITY_DATA_PATH=/data/teamcity \
    TC_PKG=TeamCity-9.1.4.tar.gz

# TeamCity data is stored in a volume to facilitate container upgrade
VOLUME  ["/data/teamcity"]

RUN wget http://download.jetbrains.com/teamcity/$TC_PKG && \
    tar zxf $TC_PKG -C /opt && \
    mv /opt/TeamCity/webapps/ROOT /opt/TeamCity/webapps/tc && \
    rm -rf $TC_PKG

# Expose Teamcity default port
EXPOSE 8111

# Default command.
CMD ["/opt/TeamCity/bin/teamcity-server.sh", "run"]
