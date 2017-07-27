FROM golang:1.8.3-alpine3.6


ENV CONTAINERPILOT_VERSION=3.1.3
ENV CONTAINERPILOT_SOURCE=https://github.com/joyent/containerpilot/releases/download/$CONTAINERPILOT_VERSION/containerpilot-$CONTAINERPILOT_VERSION.tar.gz
ENV CONTAINERPILOT=/etc/containerpilot.json
ENV CURL_VERSION 7.50.1

# Get ContainerPilot release
RUN apk add --update openssl && \
      wget $CONTAINERPILOT_SOURCE -O /tmp/cb.tar.gz  && \
      tar -xz -f /tmp/cb.tar.gz && \
      mv containerpilot /bin/
