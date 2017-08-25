FROM ubuntu:16.04
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Language settings
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

# Global packages install
# Get software properties common
RUN apt-get update && apt-get install -y --no-install-recommends \
    software-properties-common

# Get Latest Git
RUN apt-add-repository ppa:git-core/ppa

RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        cmake \
        git \
        wget \
        curl \
        bzip2 \
        nano \
        vi \
        less \
        && \
    rm -rf /var/lib/apt/lists/*
