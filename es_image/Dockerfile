FROM java_image
MAINTAINER Author name

ENV DEBIAN_FRONTEND noninteractive

VOLUME elk

RUN \
  wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.4.0.tar.gz && \
  tar xvzf elasticsearch-6.4.0.tar.gz && \
  rm -r elasticsearch-6.4.0.tar.gz && \
  mkdir -p /home/user/data && \
  chown -R user:user /home/user/data && \
  chown -R user:user elasticsearch-6.4.0 

USER user
ADD elasticsearch.yml /home/user/elasticsearch-6.4.0/config/elasticsearch.yml
ENTRYPOINT elasticsearch-6.4.0/bin/elasticsearch
