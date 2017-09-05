ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-cpu-py2
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Current available libraries
# + Theano
# + Tensorflow
# + PyTorch
# + Keras

# Install Theano
RUN conda install -y theano

# Configure Theano
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/theano/theanorc-cpu -O $HOME/.theanorc

# Install tensorflow
RUN pip install --ignore-installed --upgrade \
        https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.3.0-cp27-none-linux_x86_64.whl

# Install PyTorch
RUN conda install -y pytorch torchvision -c soumith

# Install Keras
RUN conda install -y h5py pydot graphviz
RUN pip install Keras -U

# TensorBoard support
RUN pip install tensorboard-pytorch

# Configure keras
RUN mkdir $HOME/.keras
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/keras/keras-theano.json -O $HOME/.keras/keras.json
