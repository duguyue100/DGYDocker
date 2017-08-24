FROM ubuntu:16.04
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Language settings
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

# Global packages install

# Get Latest Git
RUN apt-add-repository ppa:git-core/ppa

RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        cmake \
        git \
        && \
    rm -rf /var/lib/apt/lists/*

# Set Paths
