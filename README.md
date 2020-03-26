# turtlebot3_control PC with JACKSON_NANO
Controlling a turtlebot3 via other input(JACKSON_NANO).
-----------------------------------------------------------------------------------------------------
## Overview

This is a part of the project to control TURTLEBOT3 via ROS Melodic.

### preparatory stage

**if you already use ROS Melodic and TURTLEBOT3, pass this stage.**

First, install ARDUINO IDE

Second, Setting ARDUINO IDE

  1. In ARDUINO IDE File -> Preferences ->Additional Boards Manager URLs
      typed "https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCR/master/arduino/opencr_release/package_opencr_index.json"
      
  2. In ARDUINO IDE Tools -> Board: ~ ->Boards Manager... -> install "OpenCR by ROBOTIS"

  3. In ARDUINO IDE Tools -> Board: ~ -> select "OpenCRBoard"

  4. In ARDUINO IDE Tools -> Port: ~ -> Select Connected serial port

  5. Check firmware update 

Third, Download TURTLEBOT3 burger firmware

   1. In ARDUINO IDE File -> Examples -> TURTLEBOT3 ->TURTLEBOT3_burger -> TURTLEBOT3_core

   2. click Upload button

Fourth, Installation of TURTLEBOT3 Development Environment

Please refer to this site.
http://emanual.robotis.com/docs/en/platform/turtlebot3/ros2_setup/#hardware-setup

-----------------------------------------------------------------------------------------------------

### Usage

1. $roscore (remote PC)

2. $roslaunch turtlebot3_bringup turtlebot3_robot.launch --screen (TURTLEBOT3)

3. $roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

⚠️: Check your ROS server IP setting before use this file. (e.g. ROS_MASTER_URI, ROS_HOSTNAME in bashrc.)


if you want test file without turtlebot3

1. $roscore (remote PC)

2. $roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch --screen (remote PC)

3. $roslaunch turtlebot3_fake turtlebot3_fake.launch (remote PC)

⚠️: Check your ROS server IP setting before use this file. (e.g. ROS_MASTER_URI, ROS_HOSTNAME in bashrc.)

-----------------------------------------------------------------------------------------------------
### Requirements

1. TURTLEBOT3 burger

2. ROS Melodic

3. remote PC
