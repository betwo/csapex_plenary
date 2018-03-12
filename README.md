# CS::APEX (Algorithm Prototyper and EXperimentor for Cognitive Systems) Plenary

A central repository that points to a specific version of the core CS::APEX framework and all supported, public plugin repositories. 
This repository is meant as a means to bundle all individual and self-sustained packages into consistent releases.


## Dependencies

The project relies on the [catkin](http://wiki.ros.org/catkin) build system
developed in the [ROS](http://wiki.ros.org/) ecosystem. Many plugins also require a ROS installation.

Required for a build are:
- Linux system (tested with Ubuntu)
- C++11 compatible compiler (g++, clang++)
- Qt5 (on Ubuntu: qt5-default libqt5svg5-dev)
- libraries (included in ros-desktop):
    - boost (program_options, filesystem, system, regex)
    - [classloader](https://github.com/ros/class_loader)
    - TinyXML (on Ubuntu: libtinyxml-dev)
    - yaml-cpp (on Ubuntu: libyaml-cpp-dev)


## Basic Installation

To get the cs::APEX framework and a set of core plugins, perform the following with a working ROS setup:

    cd ~
    mkdir -p ws
    cd ws

    git clone https://github.com/betwo/csapex_plenary.git --recursive csapex

    cd csapex
    catkin_make

## Contributions

All contributions are welcome, please refer to the CONTRIBUTING.md file.
