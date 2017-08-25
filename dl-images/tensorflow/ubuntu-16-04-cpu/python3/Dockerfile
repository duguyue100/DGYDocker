ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-cpu-py3
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Install tensorflow
RUN pip3 install --ignore-installed --upgrade \
        https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.3.0-cp35-cp35m-linux_x86_64.whl

# Install Keras
RUN conda install h5py pydot graphviz
RUN pip install Keras -U

# Configure keras
RUN mkdir $HOME/.keras
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/keras/keras-tensorflow.json -O $HOME/.keras/keras.json
