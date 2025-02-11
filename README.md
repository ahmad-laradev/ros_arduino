# ROS Arduino Setup

This repository provides instructions to set up and run a ROS2-based Arduino project.

## Prerequisites

Ensure you have ROS2 installed on your system. You can follow the official ROS2 installation guide: [ROS2 Installation](https://docs.ros.org/en/)

## Step 1: Create ROS Workspace

Create and initialize the workspace:

```sh
mkdir -p arduinobot_ws/src
cd arduinobot_ws
colcon build

cd src
ros2 pkg create --build-type ament_python arduinobot_py_examples
ros2 pkg create --build-type ament_cmake arduinobot_cpp_examples
colcon build

source install/setup.bash
ros2 run arduinobot_py_examples simple_publisher
 