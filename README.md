# RIA-E100-ROBOT-PC
This is complete package that resides in robot's PC of RIA E100 ELITE

# **UPDATE : 20160626**
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
sudo apt-get install ros-kinetic-rplidar-ros ros-kinetic-astra-* ros-kinetic-twist-mux ros-kinetic-twist-mux-msgs ros-kinetic-teb-local-planner ros-kinetic-hector-mapping ros-kinetic-hector-trajectory-server ros-kinetic-map-server ros-kinetic-amcl ros-kinetic-laser-scan-matcher ros-kinetic-robot-localization ros-kinetic-imu-complementary-filter
```

*Warning*: we are going to remove entire previously installed package which is in catking_ws and will be replacing with latest files. Please backup your files if any programs done by you before doing following step. If not you can create new workspace and continue 
```
	$ cd ~/catkin_ws
	$ rm -rf /build
	$ rm -rf /devel
	$ rm -rf /src
  	$ sudo apt-get remove ros-kinetic-e100-base
	$ mkdir src
```
- Now paste downloaded file in ~/catkin_ws/src and extract it there

- Compile the latest package
```
	$ Source  /opt/ros/kinetic/setup.bash
	$ catkin_make
  	$ cd ~/catkin_make/src/ria_e100/e100_base_controller
  	$ sudo dpkg -i ros-kinetic-e100-base_0.1.0-0xenial_amd64.deb
```
- Now open bashrc file by typing `gedit .bashrc` in new terminal and make sure your bashrc is configured at the end of page as shown below

```
	export ASTRA_RGBD=true
	export RPLIDAR=true
	export SICK=false
	export IMU=true
	export USE_EKF=true

	export JOY_STICK=true
```
#### [Tutorials](https://edu.gaitech.hk/ria_e100/demo-apps.html#demo-applications) 
