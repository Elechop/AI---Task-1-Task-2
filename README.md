# AI---Task-1-Task-2
# Task 1: 

## steps of installation  Ubuntu 20.04

1- download virtualbox
 2- download Ubuntu 20.04 on linux type
 3- install Ubuntu 20.04
 4- then shut down the Ubuntu 20.04
 5- open it again and finally its ready to use

## steps of installation ROS2
- It was installed by using the commands on the ROS system website, copying it and then pasting it into Ubuntu

### Set local
>locale  # check for UTF-8
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
locale  # verify settings

### Setup Sources

>sudo apt install software-properties-common
sudo add-apt-repository universe

#### Authorize the GPG key with apt.
>sudo apt update && sudo apt install curl gnupg lsb-releasesudo curl -sSLhttps://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

#### Adding the repository to the sources list.
> echo"debarch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpghttp://packages.ros.org/ros2/ubuntu$(source /etc/os-release &&echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

### Install ROS 2 packages

>sudo apt update

>sudo apt install ros-humble-desktop

>source /opt/ros/humble/setup.bash



# Task 2: XUbuntu and ROS Installation on Jetson Nano

## Installion of XUbuntu 20.04 
1- We will download (Xubuntu 20.04 Focal Fossa L4T R32.3.1) instead of Ubuntu because it is a custom image for the Jetson Nano.
2- Using Etcher, we will flash the image on a micro SD card throgh SD Card Reader USB.

3- If our Jetson Nano was A02 then we should plug in the SD card, and after its booting, it will take us to the XUbuntu installation screen.

To find out which .dtb file is compatible with our Jetson Nano run the following on its terminal:

>cat /sys/firmware/devicetree/base/compatible

>FDT /boot/tegra210-p3448-0000-p3449-0000-b00.dtb

 ## Installion of ROS 2 Foxy Fitzroy
 
- It was installed by using the commands on packages, copying it and then pasting it into Ubuntu

>locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings

>sudo apt install software-properties-common
sudo add-apt-repository universe

>sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg

>echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

### Install ROS 2 packages
>sudo apt update

>sudo apt install ros-foxy-desktop

>source /opt/ros/foxy/setup.bash

- and by these steps the ROS system is ready to use on Jetson Nano
