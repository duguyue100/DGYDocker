# DGYDocker

Collection of my Docker files.

This repo is to host my docker files for testing and fast prototyping softwares.
The main idea is to get a full list of images that I can build flexible testing environment.
Part of this project will be used in setting up DL environment for NSC student machine.

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

## Contact

Yuhuang Hu  
Email: duguyue100@gmail.com
