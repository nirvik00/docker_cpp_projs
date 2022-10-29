FROM ubuntu:18.04
LABEL Description="Build environment"
ENV HOME /root

SHELL ["/bin/bash", "-c"]

RUN apt-get update && apt-get -y --no-install-recommends install \
    build-essential \
    clang \
    cmake \
    gdb \
    wget \
    build-essential

RUN cd ${HOME} && git clone https://github.com/oatpp/oatpp.git

RUN cd oatpp/

RUN mkdir build && \
    cd build && \
    cmake .. && \
    make install