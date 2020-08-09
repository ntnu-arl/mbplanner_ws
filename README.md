# mbplanner_ws
ROS workspace for mbplanner_ros package  

This workspace includes relevant packages to run with the [mbplanner_ros](https://github.com/unr-arl/mbplanner_ros.git).  

## Clone the package
```
git clone https://github.com/unr-arl/mbplanner_ws.git
```  

## Setup the workspace
### Ubuntu 16.04 with ROS Kinetic:  
Use the ```premerge_check_kinetic``` branch [!!!! ONLY FOR TESTING. REVERT TO master BEFORE MERGING !!!]
```bash
cd mbplanner_ws
git checkout premerge_check_kinetic ##!!!! ONLY FOR TESTING. REVERT TO master BEFORE MERGING !!!
```
### Ubuntu 18.04 with ROS Melodic:  
Use the ```premerge_check_melodic``` branch  [!!!! ONLY FOR TESTING. REVERT TO melodic-devel BEFORE MERGING !!!]
```bash
cd mbplanner_ws
git checkout premerge_check_melodic  ##!!!! ONLY FOR TESTING. REVERT TO melodic-devel BEFORE MERGING !!!
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
