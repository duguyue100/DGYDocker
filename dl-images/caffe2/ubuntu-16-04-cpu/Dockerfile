ARG repository=duguyue100/dgydocker
FROM ${repository}:base-cpu
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

RUN apt-get update && apt-get install -y --no-install-recommends \
        libgoogle-glog-dev \
        libprotobuf-dev \
        protobuf-compiler \
        libgflags-dev \
        libgflags-dev \
        libgtest-dev \
        libiomp-dev \
        libleveldb-dev \
        liblmdb-dev \
        libopencv-dev \
        libopenmpi-dev \
        libsnappy-dev \
        openmpi-bin \
        openmpi-doc \
        && \
    rm -rf /var/lib/apt/lists/*


# build and install caffe2 at /usr/local, no Python
RUN git clone --recursive https://github.com/caffe2/caffe2.git $HOME/caffe2 && cd $HOME/caffe2 \
    && mkdir build && cd build \
    && cmake .. \
    -DUSE_CUDA=OFF \
    -DUSE_NNPACK=OFF \
    -DUSE_ROCKSDB=OFF \
    -DBUILD_PYTHON=OFF \
    && make -j"$(nproc)" install \
    && ldconfig \
    && make clean \
    && cd .. \
    && rm -rf build
