# ELK-docker
An ELK example using Docker
docker build --file=logstash-dockerfile -t logstash .
docker run --rm -ti logstash /bin/bash
docker run  -t logstash
docker run  -d -p 2345:4345 -t logstash
docker kill $(docker ps -aq)
