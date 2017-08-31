ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-cpu-py2
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Install Theano
RUN conda install -y theano

# Configure Theano
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/theano/theanorc-cpu -O $HOME/.theanorc

# Install Keras
RUN conda install -y h5py pydot graphviz
RUN pip install Keras -U

# TensorBoard support
RUN pip install tensorflow-tensorboard

# Configure keras
RUN mkdir $HOME/.keras
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/keras/keras-theano.json -O $HOME/.keras/keras.json
