ARG repository=duguyue100/dgydocker
FROM ${repository}:base-cpu
LABEL maintainer "Yuhuang Hu <duguyue100@gmail.com>"

# setup python2 from Anaconda
# from ContinuumIO docker image
RUN echo 'export PATH=/opt/conda/bin:$PATH' > /etc/profile.d/conda.sh && \
    wget --quiet https://repo.continuum.io/archive/Anaconda2-4.4.0-Linux-x86_64.sh -O ~/anaconda.sh && \
    /bin/bash ~/anaconda.sh -b -p /opt/conda && \
    rm ~/anaconda.sh

ENV PATH /opt/conda/bin:$PATH

RUN conda install -y libgcc

CMD [ "/bin/bash" ]
