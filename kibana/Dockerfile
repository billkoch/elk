FROM ubuntu:14.04
RUN \
  apt-get update -y && \
  apt-get install -y wget && \
  wget https://download.elasticsearch.org/kibana/kibana/kibana-3.0.1.tar.gz && \
  mkdir -p /web/kibana && \
  tar xvf kibana-3.0.1.tar.gz -C /web/kibana && \
  cp /web/kibana/kibana-3.0.1/app/dashboards/logstash.json /web/kibana/kibana-3.0.1/app/dashboards/default.json && \
  rm -f kibana-3.0.1.tar.gz

RUN apt-get install -y python-twisted python-twisted-bin

ENTRYPOINT ["twistd", "-n", "web", "--path", "/web/kibana/kibana-3.0.1"]

EXPOSE 8080

