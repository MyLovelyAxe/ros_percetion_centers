# ros_percetion_centers

This is a collection of ROS2 humble packages which work as message exchange centers between **ROS2 topics** and **ZMQ sockets**.

The reason why is due to the conflict between the python environments for ROS2 and modern neural network models. ROS2 only runs under system python (e.g. ROS humble under Python3.10), while plenty of NN models are developed with Pytorch + CUDA under Python3.11 in virtual envs (e.g. conda env).

In order to avoid to taking much effort into make python environments of ROS2 and NN models compatible, here is a compromise, i.e. using **ZMQ sockets** as bridge to connect ROS2 under system Python3.10 and NN models under virtual env Python3.11, which doesn't reply on specific Python version.

## Collections

Here are center packages for different perception tasks, including:

- SLAM: [slam_center](https://github.com/MyLovelyAxe/slam_center)
- Object detection: [ob_center]()
- Human pose estimation: [hpe_center]()
- Segmentation: [seg_center]()

## Requirements

The ROS packages are tested on the following environment configuration:

- Ubuntu22.04
- [ROS2 humble](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)
- system python 3.10 (without virtual env)
