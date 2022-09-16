# RIA-E100-ROBOT-PC
This is complete package that resides in robot's PC of RIA E100 ELITE

**UPDATE : 20220916**
#### Description : Added features 
- Voltage and Battery capacity readings available at /e100_voltage and /e100_battery topics
- Stable controller drivers

#### Instructions to Update Latest Package
Prerequisites : Destkop with mouse and keyboard, WiFi Internet

Following steps need to be done in robot pc
- Download the latest package from [here](https://github.com/gaitech-robotics/RIA-E100-ROBOT-PC/archive/master.zip).

Install pre-requisites.

- Open the terminal by pressing keys ctrl+alt+t and type following to install dependencies  
```
sudo apt install -y python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential python-rosdep ros-melodic-rqt* ros-melodic-ros-control ros-melodic-ros-controllers ros-melodic-navigation ros-melodic-serial ros-melodic-mavros ros-melodic-rplidar-ros ros-melodic-gmapping ros-melodic-depthimage-to-laserscan ros-melodic-robot-localization ros-melodic-joy ros-melodic-teleop-twist-joy ros-melodic-teleop-twist-keyboard ros-melodic-twist-mux ros-melodic-imu-complementary-filter ros-melodic-rgbd-launch
```

*Warning*: we are going to remove entire previously installed package which is in catking_ws and will be replacing with latest files. Please backup your files if any programs done by you before doing following step. If not you can create new workspace and continue 
```
	$ mkdir -p ~/catkin_ws/src
	$ cd ~/catkin_ws/src && catkin_init_workspace
```
- Now paste downloaded file in ~/catkin_ws/src and extract it there
```
	$ cd ~/catkin_ws/src && git clone https://github.com/gaitech-robotics/RIA-E100-ROBOT-PC.git
```
- Compile the latest package
```
	$ source  /opt/ros/melodic/setup.bash
	$ cd ~/catkin_ws && catkin_make
  	$ cd ~/catkin_make/src/ria_e100/e100_base_controller
  	$ sudo dpkg -i ros-melodic-e100-base_0.1.0-0bionic_amd64.deb
```
#### [Tutorials](https://edu.gaitech.hk/ria_e100/demo-apps.html#demo-applications) 
