# turtlebot3_remote_control
Controlling a turtlebot via other input.
-----------------------------------------------------------------------------------------------------
Overview
This is a part of the project to control Turtlebot3 via ROS Melodic.

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

Fourth,  

http://emanual.robotis.com/docs/en/platform/turtlebot3/ros2_setup/#hardware-setup

----------------------------------------------------------------------------------------------------

How to control turtlebot3 speed?

directory: HOME -> catkin_ws -> src -> turtlebot3 -> turtlebot3_teleop -> nodes ->turtlelbot3_teleop_key

Change a value of LIN_VEL_STEP_SIZE and ANG_VEL_STEP_SIZE

How we can change turtlebot3 control button?

directory: HOME -> catkin_ws -> src -> turtlebot3 -> turtlebot3_teleop -> nodes ->turtlelbot3_teleop_key

Change a value of key

-----------------------------------------------------------------------------------------------------

How we can connect between PCs through ROS?

When we connect between PCs, we can't use 2 roscore. So we have to change value of ROS_MASTER_URI

directory of ROS_MASTER_URI : In terminal typed"gedit ~/.bashrc" -> Change value of ROS_MASTER_URI

-----------------------------------------------------------------------------------------------------
Requirements
turtlebot3 burger
ROS Melodic
remote PC
