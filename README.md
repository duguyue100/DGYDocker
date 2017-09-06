# [DGYDocker](https://github.com/duguyue100/DGYDocker)

Collection of my Docker files.

This repo is to host my docker files for testing and fast prototyping softwares.
The main idea is to get a full list of images that I can build flexible testing environment.
Part of this project will be used in setting up DL environment for NSC student machine.

## List of Images

### CPU

|Base Image|Deep Learning Base|Theano|TensorFlow|PyTorch|
|:---------|:-----------------|:-----|:---------|:------|
|[base-cpu](./base/ubuntu-16-04-cpu)|[dl-base-cpu-py2](./dl-images/dl-base/ubuntu-16-04-cpu/python2)|[dl-th-cpu-py2](./dl-images/theano/ubuntu-16-04-cpu/python2)|[dl-tf-cpu-py2](./dl-images/tensorflow/ubuntu-16-04-cpu/python2)|[dl-pt-cpu-py2](./dl-images/pytorch/ubuntu-16-04-cpu/python2)|
|[base-16-04-cpu](./base/ubuntu-16-04-cpu)|[dl-base-cpu-py3](./dl-images/dl-base/ubuntu-16-04-cpu/python3)|[dl-th-cpu-py3](./dl-images/theano/ubuntu-16-04-cpu/python3)|[dl-tf-cpu-py3](./dl-images/tensorflow/ubuntu-16-04-cpu/python3)|[dl-pt-cpu-py3](./dl-images/pytorch/ubuntu-16-04-cpu/python3)|
||[dl-base-16-04-cpu-py2](./dl-images/dl-base/ubuntu-16-04-cpu/python2)|[dl-th-16-04-cpu-py2](./dl-images/theano/ubuntu-16-04-cpu/python2)|[dl-th-16-04-cpu-py2](./dl-images/tensorflow/ubuntu-16-04-cpu/python2)|[dl-pt-16-04-cpu-py2](./dl-images/pytorch/ubuntu-16-04-cpu/python2)|
||[dl-base-16-04-cpu-py3](./dl-images/dl-base/ubuntu-16-04-cpu/python3)|[dl-th-16-04-cpu-py3](./dl-images/theano/ubuntu-16-04-cpu/python3)|[dl-th-16-04-cpu-py3](./dl-images/tensorflow/ubuntu-16-04-cpu/python3)|[dl-pt-16-04-cpu-py3](./dl-images/pytorch/ubuntu-16-04-cpu/python3)|
|__Caffe__|__Caffe2__|__DMLC__|__Torch__|__FULL__|
|[dl-cf-cpu](./dl-images/caffe/ubuntu-16-04-cpu)|[dl-c2-cpu](./dl-images/caffe2/ubuntu-16-04-cpu)|[dl-dmlc-cpu-py2](./dl-images/dmlc/ubuntu-16-04-cpu/python2)|[dl-tr-cpu](./dl-images/torch/ubuntu-16-04-cpu)|[dl-full-cpu-py2](./dl-images/full/ubuntu-16-04-cpu/python2)|
|[dl-cf-16-04-cpu](./dl-images/caffe/ubuntu-16-04-cpu)|[dl-c2-16-04-cpu](./dl-images/caffe2/ubuntu-16-04-cpu)|[dl-dmlc-cpu-py3](./dl-images/dmlc/ubuntu-16-04-cpu/python3)|[dl-tr-16-04-cpu](./dl-images/torch/ubuntu-16-04-cpu)|[dl-full-cpu-py3](./dl-images/full/ubuntu-16-04-cpu/python3)|
|         |          |[dl-dmlc-16-04-cpu-py2](./dl-images/dmlc/ubuntu-16-04-cpu/python2)|         |[dl-full-16-04-cpu-py2](./dl-images/full/ubuntu-16-04-cpu/python2)|
|         |          |[dl-dmlc-16-04-cpu-py3](./dl-images/dmlc/ubuntu-16-04-cpu/python3)|         |[dl-full-16-04-cpu-py3](./dl-images/full/ubuntu-16-04-cpu/python3)|

### GPU

|Base Image|Deep Learning Base|Theano|TensorFlow|PyTorch|
|:---------|:-----------------|:-----|:---------|:------|
|[base-gpu](./base/ubuntu-16-04-gpu)|[dl-base-gpu-py2](./dl-images/dl-base/ubuntu-16-04-gpu/python2)|[dl-th-gpu-py2](./dl-images/theano/ubuntu-16-04-gpu/python2)|[dl-tf-gpu-py2](./dl-images/tensorflow/ubuntu-16-04-gpu/python2)|[dl-pt-gpu-py2](./dl-images/pytorch/ubuntu-16-04-gpu/python2)|
|[base-16-04-gpu](./base/ubuntu-16-04-gpu)|[dl-base-gpu-py3](./dl-images/dl-base/ubuntu-16-04-gpu/python3)|[dl-th-gpu-py3](./dl-images/theano/ubuntu-16-04-gpu/python3)|[dl-tf-gpu-py3](./dl-images/tensorflow/ubuntu-16-04-gpu/python3)|[dl-pt-gpu-py3](./dl-images/pytorch/ubuntu-16-04-gpu/python3)|
||[dl-base-16-04-gpu-py2](./dl-images/dl-base/ubuntu-16-04-gpu/python2)|[dl-th-16-04-gpu-py2](./dl-images/theano/ubuntu-16-04-gpu/python2)|[dl-th-16-04-gpu-py2](./dl-images/tensorflow/ubuntu-16-04-gpu/python2)|[dl-pt-16-04-gpu-py2](./dl-images/pytorch/ubuntu-16-04-gpu/python2)|
||[dl-base-16-04-gpu-py3](./dl-images/dl-base/ubuntu-16-04-gpu/python3)|[dl-th-16-04-gpu-py3](./dl-images/theano/ubuntu-16-04-gpu/python3)|[dl-th-16-04-gpu-py3](./dl-images/tensorflow/ubuntu-16-04-gpu/python3)|[dl-pt-16-04-gpu-py3](./dl-images/pytorch/ubuntu-16-04-gpu/python3)|
|__Caffe__|__Caffe2__|__DMLC__|__Torch__|__FULL__|
|[dl-cf-gpu](./dl-images/caffe/ubuntu-16-04-gpu)|[dl-c2-gpu](./dl-images/caffe2/ubuntu-16-04-gpu)|[dl-dmlc-gpu-py2](./dl-images/dmlc/ubuntu-16-04-gpu/python2)|         |[dl-full-gpu-py2](./dl-images/full/ubuntu-16-04-gpu/python2)|
|[dl-cf-16-04-gpu](./dl-images/caffe/ubuntu-16-04-gpu)|[dl-c2-16-04-gpu](./dl-images/caffe2/ubuntu-16-04-gpu)|[dl-dmlc-gpu-py3](./dl-images/dmlc/ubuntu-16-04-gpu/python3)|         |[dl-full-gpu-py3](./dl-images/full/ubuntu-16-04-gpu/python3)|
|         |          |[dl-dmlc-16-04-gpu-py2](./dl-images/dmlc/ubuntu-16-04-gpu/python2)|         |[dl-full-16-04-gpu-py2](./dl-images/full/ubuntu-16-04-gpu/python2)|
|         |          |[dl-dmlc-16-04-gpu-py3](./dl-images/dmlc/ubuntu-16-04-gpu/python3)|         |[dl-full-16-04-gpu-py3](./dl-images/full/ubuntu-16-04-gpu/python3)|

## Design Principles

+ Everything is with Ubuntu LTS, starting from 16.04.
+ Anaconda Python as the default python.
+ Base image install only necessary packages for all images.
+ `dl-base` dockerfile supports only necessary C/C++ and Python compilation.

## Planned Image

+ [ ] Base Image that contains all essential building tools
+ [ ] DL Image for TensorFlow class (gpu/cpu)
+ [ ] DL Image for Theano class (gpu/cpu)
+ [ ] DL Image for Caffe class (gpu/cpu)
+ [ ] DL Image for Torch class (gpu/cpu)
+ [ ] Full DL Image (gpu/cpu)
+ [ ] AER Processing Image
+ [ ] DL AER Image (gpu/cpu)
+ [ ] AER ROS Image

## Related Resources

+ [NVIDIA Dockerfiles](https://gitlab.com/nvidia/cuda)
+ [Caffe Dockerfiles](https://github.com/BVLC/caffe/tree/master/docker)
+ [ROS Dockerfiles](https://github.com/osrf/docker_images/tree/7ba58fc107b368d6409c22161070eb93e562f240/ros)
+ [Anaconda Dockerfiles](https://github.com/ContinuumIO/docker-images)

## Notes

1. From the test, it seems that `theano` on CPU container is much slower than my native run on Mac.
Not sure if it's also true on Linux.

## Contact

Yuhuang Hu  
Email: duguyue100@gmail.com
