# -*- mode: dockerfile -*-
# vi: set ft=dockerfile :

FROM ubuntu:xenial
WORKDIR /drake
COPY setup/ubuntu setup/ubuntu
RUN set -eux \
  && export DEBIAN_FRONTEND=noninteractive \
  && yes | setup/ubuntu/install_prereqs.sh \
  && rm -rf /var/lib/apt/lists/*
COPY . .
ENTRYPOINT ["./setup/ubuntu/docker/entrypoint.sh"]
