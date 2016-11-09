#Ubuntu install of ROS Kinetic
##step
#1.1 Configure your Ubuntu repositories
Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." 
#1.2 Setup your sources.list
Setup your computer to accept software from packages.ros.org. ROS Kinetic ONLY supports Wily (Ubuntu 15.10), Xenial (Ubuntu 16.04) and Jessie (Debian 8) for debian packages. 

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
#1.3 Set up your keys
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
#1.4 Installation
sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic
#1.5 Initialize rosdep
sudo rosdep init

rosdep update
#1.6 Environment setup
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc

source ~/.bashrc
#1.7 Getting rosinstall
sudo apt-get install python-rosinstall

