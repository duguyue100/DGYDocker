ARG repository=duguyue100/dgydocker
FROM ${repository}:base-gpu
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

RUN apt-get update && apt-get install -y --no-install-recommends \
        libatlas-base-dev \
        libboost-all-dev \
        libgflags-dev \
        libgoogle-glog-dev \
        libhdf5-serial-dev \
        libleveldb-dev \
        liblmdb-dev \
        libopencv-dev \
        libprotobuf-dev \
        libsnappy-dev \
        protobuf-compiler \
        && \
    rm -rf /var/lib/apt/lists/*

ENV CAFFE_ROOT=/opt/caffe
WORKDIR $CAFFE_ROOT

RUN git clone -b 1.0 --depth 1 https://github.com/BVLC/caffe.git . && \
    git clone https://github.com/NVIDIA/nccl.git && cd nccl && make -j install && cd .. && rm -rf nccl && \
    mkdir build && cd build && \
    cmake -DUSE_CUDNN=1 -DUSE_NCCL=1 -DBUILD_python=0 -DBUILD_python_layer=0 .. && \
    make -j"$(nproc)"


ENV PATH $CAFFE_ROOT/build/tools:$PATH
RUN echo "$CAFFE_ROOT/build/lib" >> /etc/ld.so.conf.d/caffe.conf && ldconfig
