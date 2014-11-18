A simple ELK stack demo that ingests log messages from RabbitMQ and outputs them to ElasticSearch.  Which leverages Docker containers managed by Fig.

Getting started:
<ol>
  <li>Install Docker:  https://docs.docker.com/installation/#installation</li>
  <li>Install Fig:  http://www.fig.sh/install.html (I recommend leveraging `pip install ...`)</li>
  <li>`git clone git@github.com:billkoch/elk`</li>
  <li>`fig up`</li>
</ol>

The RabbitMQ Admin UI is configured via fig.yml to be available @ http://localhost:15672 (by default)
The Kibana front-end for ElasticSearch is configured via fig.yml to be available @ http://localhost:80 (by default)
