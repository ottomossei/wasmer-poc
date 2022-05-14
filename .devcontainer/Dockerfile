# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.217.2/containers/cpp/.devcontainer/base.Dockerfile

# [Choice] Debian / Ubuntu version (use Debian 11, Ubuntu 18.04/21.04 on local arm64/Apple Silicon): debian-11, debian-10, ubuntu-21.04, ubuntu-20.04, ubuntu-18.04
ARG VARIANT="bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/cpp:0-${VARIANT}

# Prepare Cpp environment
RUN apt-get update && \
    apt-get install -y g++ rsync zip openssh-server make 

# Prepare Wasmer
RUN apt-get update && \
    apt-get install -y curl libxkbcommon-x11-0 libncurses5
RUN curl https://get.wasmer.io -sSfL | sh

ENV WASMER_DIR ${HOME}/.wasmer
ENV PATH ${WASMER_DIR}/bin:${PATH}

RUN echo $PATH

# [Optional] Uncomment this section to install additional packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
VOLUME "~/.ssh:.ssh"
VOLUME "~/.gitconfig:.gitconfig"

CMD /bin/bash
