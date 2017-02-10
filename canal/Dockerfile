FROM wurstmeister/base
ENV JAVA_HOME /usr/lib/jvm/java-7-openjdk-amd64

ADD https://github.com/alibaba/canal/releases/download/v1.0.23/canal.deployer-1.0.23.tar.gz /tmp/canal.tar.gz
RUN cd /tmp/ && mkdir canal && tar -zxvf canal.tar.gz -C /tmp/canal
WORKDIR /tmp/canal
RUN cd /tmp/canal/bin
CMD bash /tmp/canal/bin/startup.sh && tail -f /tmp/canal/logs/canal/canal.log
