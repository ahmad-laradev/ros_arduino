# ros_arduino

## Step: 1
 
 Create ROS workspace :
    $ mkdir -p arduinobot_ws/src
    $ cd arduinobot_ws
    $ colcon build

 Package template creation :
    $ cd src
    $ ros2 pkg create --build-type ament_python arduinobot_py_examples
    $ ros2 pkg create --build-type ament_cmake arduinobot_cpp_examples
    $ colcon build
 Run code :
    $ colcon build
    $ ros2 run arduinobot_py_examples simple_publisher
 