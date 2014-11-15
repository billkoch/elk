FROM ubuntu:14.04

RUN \
  apt-get update -y && \
  apt-get install -y wget && \
  wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch | apt-key add - && \
  echo "deb http://packages.elasticsearch.org/logstash/1.4/debian stable main" >> /etc/apt/sources.list && \
  apt-get update -y && \
  apt-get install -y logstash

RUN \
  mkdir -p /opt/logstash/conf && \
  echo "input { stdin { } } output { stdout {} }" > /opt/logstash/conf/logstash.conf

VOLUME ["/opt/logstash/conf"]

ENTRYPOINT ["/opt/logstash/bin/logstash"]
CMD ["--config", "/opt/logstash/conf/logstash.conf"]
