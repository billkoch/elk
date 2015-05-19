A simple ELK stack demo that ingests log messages from RabbitMQ and outputs them to ElasticSearch.  Which leverages Docker containers managed by Docker-Compose.

Getting started:
<ol>
  <li>Install Docker:  https://docs.docker.com/installation/#installation</li>
  <li>Install Docker-Compose: https://docs.docker.com/compose/install/#install-compose (I recommend leveraging `pip install ...`)</li>
  <li>`git clone git@github.com:billkoch/elk`</li>
  <li>`docker-compose up`</li>
</ol>

<ul>
  <li>The RabbitMQ Admin UI is configured via docker-compose.yml to be available @ http://localhost:15672 (by default)</li>
  <li>The Kibana front-end for ElasticSearch is configured via docker-compose.yml to be available @ http://localhost:80 (by default)</li>
</ul>
