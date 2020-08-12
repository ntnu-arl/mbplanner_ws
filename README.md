# mbplanner_ws
ROS workspace for mbplanner_ros package  

This workspace includes relevant packages to run with the [mbplanner_ros](https://github.com/unr-arl/mbplanner_ros.git).  

## Clone the package
```
git clone https://github.com/unr-arl/mbplanner_ws.git
```  

## Setup the workspace
### Ubuntu 16.04 with ROS Kinetic:  
#### If gazebo 7.x or 8.x is used:
Use the ```master``` branch
```bash
cd mbplanner_ws
```
#### If gazebo 9.x is used:
Use the ```melodic-devel``` branch  
```bash
cd mbplanner_ws
git checkout melodic-devel
```  
### Ubuntu 18.04 with ROS Melodic:  
Use the ```melodic-devel``` branch  
```bash
cd mbplanner_ws
git checkout melodic-devel
```
### Clone required packages
```bash
wstool init
# https:
wstool merge packages_https.rosinstall
# ssh: use following command to clone using ssh
# wstool merge packages_ssh.rosinstall
wstool update
```

### Build the whole workspace
```
catkin config -DCMAKE_BUILD_TYPE=Release
catkin build
````
