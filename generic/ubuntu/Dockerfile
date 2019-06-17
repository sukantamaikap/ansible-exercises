FROM ubuntu:18.04

EXPOSE 22 8088 50070

RUN apt-get -y update \
    && apt-get install -y \ 
    iputils-ping \
    openssh-server

CMD service ssh start && while true; do sleep 3000; done