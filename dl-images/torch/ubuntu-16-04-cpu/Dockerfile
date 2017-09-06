ARG repository=duguyue100/dgydocker
FROM ${repository}:base-cpu
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

RUN git clone https://github.com/torch/distro.git $HOME/torch --recursive &&
    cd $HOME/torch &&
    bash install-deps &&
    ./install.sh -b

RUN rm -rf /var/lib/apt/lists/*
