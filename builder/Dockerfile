#
# Licensed under Apache License v2. See LICENSE for more information.
#


FROM alpine:3.3
MAINTAINER Pepijn Noltes <pepijnnoltes@gmail.com>

ENV CELIX_BRANCH develop
ENV CELIX_CMAKE_OPTIONS "" #TODO BUILD_ options
ENV CELIX_NINJA_OPTIONS ""

RUN apk add --update \
    build-base \
    cmake \
    ninja \
    alpine-sdk \
    git \
    vim

RUN apk add --update \
    curl-dev \
    libuuid \
    util-linux-dev \
    libffi-dev \
    jansson-dev \
    bsd-compat-headers \
    openjdk8 

RUN ln -s /usr/lib/jvm/default-jvm/jar /usr/bin/jar 
    
RUN cd /root && git clone --single-branch -b ${CELIX_BRANCH} https://github.com/apache/celix.git celix-src

ADD APKBUILD /root

#RUN cd /root && abuild -F build`
