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
#### Enable the Ubuntu Universe repository
>sudo apt install software-properties-common
sudo add-apt-repository universe

#### Authorize the GPG key with apt.
>sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

#### Adding the repository to the sources list.
> echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

### Install ROS 2 packages

>sudo apt update

>sudo apt install ros-humble-desktop

>source /opt/ros/humble/setup.bash



# Task 2: 
