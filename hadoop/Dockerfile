FROM sequenceiq/hadoop-docker:2.7.1

ADD bootstrap.sh /etc/
ADD core-site.xml hdfs-site.xml /usr/local/hadoop/etc/hadoop/
ADD log4j.properties /usr/local/hadoop/etc/hadoop/

RUN mkdir -p /scripts /opt/hadoop
ADD waitfor.sh /scripts/
RUN chmod 777 /scripts/waitfor.sh

VOLUME ["/data"]

RUN useradd -u 1000 -s /bin/bash -m -d /home/rstudio rstudio

# CMD ["/etc/bootstrap.sh"]
