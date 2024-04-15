FROM ubuntu:24.04

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends bundler git locales curl

RUN locale-gen en_GB.UTF-8
ENV LANG en_GB.UTF-8

RUN bash -c 'curl https://raw.githubusercontent.com/leanprover/elan/master/elan-init.sh -sSf | sh -s -- -y --default-toolchain leanprover/lean4:stable

ENV PATH="${PATH}:/root/.elan/bin"
