ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-cpu-py3
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Current available libraries
# + Theano
# + Tensorflow
# + PyTorch
# + Keras
# + DMLC
# + Caffe 2
# + Caffe

### Theano

# Install Theano
RUN conda install -y theano

# Configure Theano
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/theano/theanorc-cpu -O $HOME/.theanorc

### TensorFlow ###

# Install tensorflow
RUN pip install --ignore-installed --upgrade \
        https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.3.0-cp36-cp36m-linux_x86_64.whl

### PyTorch ###

# Install PyTorch
RUN conda install -y pytorch torchvision -c soumith

### Keras ###

# Install Keras
RUN conda install -y h5py
# RUN pip install pydot==1.1.0
RUN pip install Keras -U

# TensorBoard support
RUN pip install tensorboard-pytorch

# Configure keras
RUN mkdir $HOME/.keras
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/keras/keras-theano.json -O $HOME/.keras/keras.json

### DMLC ####

# Install Xgboost and mxnet
RUN pip install xgboost mxnet==0.11.0.rc3

### Caffe2 ###

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

### Caffe ###

RUN apt-get update && apt-get install -y --no-install-recommends \
        libatlas-base-dev \
        libboost-all-dev \
        libhdf5-serial-dev \
        && \
    rm -rf /var/lib/apt/lists/*

ENV CAFFE_ROOT=/opt/caffe
WORKDIR $CAFFE_ROOT

# build and install caffe, no Python
RUN git clone -b 1.0 --depth 1 https://github.com/BVLC/caffe.git . && \
    mkdir build && cd build && \
    cmake -DCPU_ONLY=1 -DBUILD_python=0 -DBUILD_python_layer=0 .. && \
    make -j"$(nproc)"

ENV PATH $CAFFE_ROOT/build/tools:$PATH
RUN echo "$CAFFE_ROOT/build/lib" >> /etc/ld.so.conf.d/caffe.conf && ldconfig
