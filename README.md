# mbplanner_ws
This workspace includes relevant packages to run with the [mbplanner_ros](https://github.com/MihirDharmadhikari/mbplanner_ros.git).  

## Clone the package
```
git clone https://github.com/MihirDharmadhikari/mbplanner_ws.git
```  

## Setup the workspace
### Ubuntu 16.04 with ROS Kinetic:  
Use the ```master``` branch  
```bash
cd mbplanner_ws
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

The whole workspace has been tested in Ubuntu 16.04 and ROS Kinetic. We will test and update further with respect to Ubuntu18 and ROS-Melodic.
