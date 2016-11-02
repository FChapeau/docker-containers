FROM jenkinsci/jnlp-slave
MAINTAINER Francois Drouin-Morin

RUN apt-get update
RUN apt-get install apt-transport-https ca-certificates -y
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
COPY docker.list /etc/apt/sources.list.d
RUN apt-get update
RUN apt-get purge lxc-docker
RUN apt-get install docker-engine -y
