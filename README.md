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
ros2 pkg create --build-type ament_python ros_arduino
ros2 pkg create --build-type ament_cmake ros_arduino_cpp
colcon build

source install/setup.bash
ros2 run ros_arduino simple_publisher

ros2 topic list
ros2 topic echo /chatter
ros2 topic info /chatter --verbose
ros2 topic hz /chatter
ros2 topic pub /chatter std_msgs/msg/String "data: 'Hassan here Ros2'"
