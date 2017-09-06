ARG repository=duguyue100/dgydocker
FROM ${repository}:dl-base-gpu-py3
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# Install PyTorch
RUN conda install -y pytorch torchvision cuda80 -c soumith

# TensorBoard support
RUN pip install tensorflow-tensorboard
RUN pip install tensorboard-pytorch
