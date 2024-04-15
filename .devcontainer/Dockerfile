FROM ubuntu:24.04

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends bundler wget unzip git locales

RUN locale-gen en_GB.UTF-8
ENV LANG en_GB.UTF-8

RUN cd /opt && wget https://github.com/leanprover/lean4/releases/download/v4.7.0/lean-4.7.0-linux.zip && unzip lean-4.7.0-linux.zip && rm -f lean-4.7.0-linux.zip

ENV PATH="${PATH}:/opt/lean-4.7.0-linux/bin"
