FROM ubuntu:focal
MAINTAINER Ystinia Zalatova (https://github.com/ystinia)
LABEL description="Experiments with Nimble Streamer"

RUN apt-get update -y \
    && apt-get install -y apt-utils curl gnupg sudo

RUN echo "deb http://nimblestreamer.com/ubuntu focal/" >> /etc/apt/sources.list \
    && curl -L -s http://nimblestreamer.com/gpg.key | apt-key add - \
    && apt-get update -y \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y nimble  \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENV TZ=Europe/Rome
RUN sudo ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

VOLUME /etc/nimble
VOLUME /var/cache/nimble

ADD files/nimble.conf /etc/nimble/nimble.conf
ADD files/rules.conf /etc/nimble/rules.conf

# EXPOSE 554 1935 8000 8181

ENTRYPOINT ["/usr/bin/nimble", "--conf-dir=/etc/nimble", "--log-dir=/var/log/nimble","--pidfile=/var/run/nimble.pid"]
