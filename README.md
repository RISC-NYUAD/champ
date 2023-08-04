
# champ [![Build Status](https://travis-ci.org/chvmp/champ.svg?branch=master)](https://travis-ci.org/chvmp/champ) 
ROS Packages for CHAMP Quadruped Controller.

## 1. Installation

### 1.1 Clone and install all dependencies:

    sudo apt install -y python-rosdep
    cd <your_ws>/src
    git clone --recursive git@github.com:RISC-NYUAD/champ.git
    git checkout fastlio
    cd ..
    rosdep install --from-paths src --ignore-src -r -y
    catkin build


    roslaunch spot_config gazebo.launch

Definitely need to hit ***ctrl+shift+R*** once, to reset the robot standing up

Accepts linear xy and angular z velocities at topic /cmd_vel
Accepts a quaternion and a z position at topic /body_pose
***z position should change smoothly to avoid jumps***
