FROM ubuntu:xenial
MAINTAINER Author name
 
RUN apt-get update
RUN apt-get install -y python-software-properties software-properties-common
RUN \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get install -y oracle-java8-installer

RUN useradd -d /home/user -m user
WORKDIR /home/user
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
