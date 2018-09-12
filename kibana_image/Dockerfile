FROM java_image
MAINTAINER Author name

ENV DEBIAN_FRONTEND noninteractive

RUN \
  wget https://artifacts.elastic.co/downloads/kibana/kibana-6.4.0-linux-x86_64.tar.gz && \
  tar xvfz kibana-6.4.0-linux-x86_64.tar.gz && \
  rm -f kibana-6.4.0-linux-x86_64.tar.gz && \
  chown -R user:user kibana-6.4.0-linux-x86_64

ADD kibana.yml kibana-6.4.0-linux-x86_64/config/kibana.yml

CMD kibana-6.4.0-linux-x86_64/bin/kibana
