# Setting-up-Ubuntu-Rpi-Properly
Troubleshooting info to set up Ubuntu 22.04.4 LTS (Jammy Jellyfish) on Rasbperry Pi for ROS2 (Humble) work and PX4 stack Via Telem2 Port on Pixhawk 6X Board 

# 2024 Version
## Preliminary Setup
0. Set up the pixhawk board for communication with these [instructions](https://docs.px4.io/v1.14/en/companion_computer/pixhawk_rpi.html#ros-2-and-uxrce-dds) (I will make a separate instruciton file to set up the pixhawk board properly for the Holybro X500 V2 using proper QGroundCOntrol Version, flight settings, and Radio Setup)
1. If using Rpi, install Ubuntu on it using these [instructions](https://docs.px4.io/v1.14/en/companion_computer/pixhawk_rpi.html#ubuntu-setup-on-rpi).
2. Then get it prepared for connection to Pixhawk Board [here](https://ubuntu.com/tutorials/how-to-install-ubuntu-desktop-on-raspberry-pi-4#1-overview)
3. Install [ROS2 Humble](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)
4. Install the MicroRTPS Agent to connect to topics from Pixhawk Board
5. Set up wiring cables using these [instructions](https://docs.px4.io/v1.14/en/companion_computer/pixhawk_rpi.html#wiring)
6. Follow these [instructions](https://docs.px4.io/v1.14/en/ros/ros2_comm.html#build-ros-2-workspace) to set up a ROS2 workspace that contains PX4 message definitions as well as some example code for working with PX4 stack and run the [example](https://docs.px4.io/v1.14/en/ros/ros2_comm.html#running-the-example) to make sure it all works

   
## Troubleshooting for Running Everything Smoothly with ROS and PX4
1. Get the package you want to run from your github and put it in your [ros_ws_name]/src/ and then go back to root
2. You're going to want to use Conda to keep your dependencies in order. Conda **miniforge** which emphasises supporting various CPU architectures like _aarch64_ which is what the Raspberry Pi 4 Model B uses (you can check this using the "uname -m" command in bash shell). Install miniforge from the instructions [here](https://github.com/conda-forge/miniforge?tab=readme-ov-file#install) (I like the curl instructions).
3. 

