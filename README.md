 #[ROS1-Download-Instructions]
 Instructions for downloading and installing ROS1

 #ROS1 Download and Installation Instructions

 #Overview
ROS (Robot Operating System) is a flexible framework for writing robot software. This guide will walk you through downloading and installing ROS1 on Ubuntu.

 #Prerequisites
-Ubuntu 20.04 (Focal)
-Ensure your system is up-to-date:
  sudo apt update 
  sudo apt upgrade 

#Step 1: Set up your sources.list

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
 

#Step 2: Set up your keys

sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

#Step 3: Installation

sudo apt update

#[you have 3 recommended options]

#1-Desktop-Full Install:
sudo apt install ros-noetic-desktop-full

#2-Desktop Install:
sudo apt install ros-noetic-desktop

#3-ROS-Base: (Bare Bones)
sudo apt install ros-noetic-ros-base


#Step 4: Initialize rosdep

sudo rosdep init
rosdep update

#Step 5: Environment setup

echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

#[If you have more than one ROS distribution installed, use this command:]
source /opt/ros/noetic/setup.bash

#Step 6: Dependencies for building packages

sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

#now You can proceed to create and manage your ROS projects;)

