ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-gpu-py3
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Install tensorflow
RUN pip install --ignore-installed --upgrade \
        https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.3.0-cp36-cp36m-linux_x86_64.whl

# Install Keras
RUN conda install -y h5py pydot graphviz
RUN pip install Keras -U

# Configure keras
RUN mkdir $HOME/.keras
RUN wget --quiet https://raw.githubusercontent.com/duguyue100/DGYDocker/master/extras/keras/keras-tensorflow.json -O $HOME/.keras/keras.json
