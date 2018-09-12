FROM java_image
MAINTAINER Author name

ENV DEBIAN_FRONTEND noninteractive

RUN \
  wget https://artifacts.elastic.co/downloads/logstash/logstash-6.4.0.tar.gz && \
  tar xvfz logstash-6.4.0.tar.gz && \
  rm -f logstash-6.4.0.tar.gz && \
  chown -R user:user logstash-6.4.0

ADD logstash.conf /home/user

CMD logstash-6.4.0/bin/logstash -f logstash.conf --verbose
