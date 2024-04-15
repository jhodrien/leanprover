ARG VARIANT="jammy"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -yq build-essential nodejs npm

RUN locale-gen en_GB.UTF-8
ENV LANG en_GB.UTF-8

USER vscode

RUN curl https://raw.githubusercontent.com/leanprover/elan/master/elan-init.sh -sSf | sh -s -- -y --default-toolchain leanprover/lean4:stable

RUN echo 'export PATH="$HOME/.elan/bin:$PATH"' >> $HOME/.profile
