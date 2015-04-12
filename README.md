# ELK-docker
An ELK example using Docker
docker build --file=logstash-dockerfile -t cdelgehier/logstash .
docker run --rm -ti cdelgehier/logstash /bin/bash
docker run  -d -p 2345:4345 -t cdelgehier/logstash
docker kill $(docker ps -aq)
docker run -d -P -c="1" -m "128m" -t cdelgehier/logstash
docker build --file="elasticsearch-dockerfile" -t cdelgehier/elasticsearch .
docker run -d -p 9200:9200 -p 9300:9300 -v "$PWD/config":/usr/share/elasticsearch/config -v "$PWD/esdata":/usr/share/elasticsearch/data cdelgehier/elasticsearch
docker build --file="kibana-dockerfile" -t cdelgehier/kibana .
