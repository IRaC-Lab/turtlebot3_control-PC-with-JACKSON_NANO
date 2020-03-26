# turtlebot3_remote_control
Controlling a turtlebot via other input.
-----------------------------------------------------------------------------------------------------
Overview
This is a part of the project to control Turtlebot3 via ROS Melodic.

#### preparatory stage

**if you aleady use ROS Melodic and turtlebot3, you can pass this stage.**

First, install arduino IDE

Second, Setting arduino IDE

  1. In arduino IDE File -> Preferences ->Additional Boards Manager URLs
      typed "https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCR/master/arduino/opencr_release/package_opencr_index.json
      
  2. In arduino IDE Tools -> Board: ~ ->Boards Manager... -> install "OpenCR by ROBOTIS"

  3. In arduino IDE Tools -> Board: ~ -> select "OpenCRBoard"

  4.In arduino IDE Tools -> Port: ~ -> Select Connected serial port

  5. Check firmware update 

Third, Download turtlebot3 burger firmware

   1.In arduino IDE File -> Examples -> turtlebot3 ->turtlebot3_burger -> turtlebot3_core

   2.click Upload button

Fourth, Installation of Turtlebot 3 Development Environment

Please refer to this site.
http://emanual.robotis.com/docs/en/platform/turtlebot3/ros2_setup/#hardware-setup

-----------------------------------------------------------------------------------------------------

#### Usage

1. $roscore (remote PC)

2. $roslaunch turtlebot3_bringup turtlebot3_robot.launch --screen (turtlebot3)

3. $roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

if you want test file without turtlebot3

1. $roscore (remote PC)

2. $roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

3. $roslaunch turtlebot3_fake turtlebot3_fake.launch (remote PC)

-----------------------------------------------------------------------------------------------------
#### Requirements

turtlebot3 burger

ROS Melodic

remote PC
