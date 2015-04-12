# ELK-docker
An ELK example using Docker
docker build --file=logstash-dockerfile -t cdelgehier/logstash .
docker run --rm -ti cdelgehier/logstash /bin/bash
docker run  -d -p 2345:4345 -t cdelgehier/logstash
docker kill $(docker ps -aq)
docker run -d -P -c="1" -m "128m" -t cdelgehier/logstash
