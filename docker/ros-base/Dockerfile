FROM ubuntu:16.04

RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
RUN apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116

RUN apt-get update \
    && apt-get install -y ros-lunar-desktop-full \
    && apt-get install -y python-rosinstall python-rosinstall-generator python-wstool build-essential \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rosdep init
RUN rosdep update

RUN echo "source /opt/ros/lunar/setup.bash" >> ~/.bashrc


