ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-cpu-py2
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Install tensorflow
RUN pip install --ignore-installed --upgrade \
        https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.3.0-cp27-none-linux_x86_64.whl

# Install Keras
RUN conda install h5py pydot graphviz

# Configure keras
RUN mkdir $HOME/.keras
