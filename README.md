# mbplanner_ws
ROS workspace for mbplanner_ros package  

This workspace includes relevant packages to run [mbplanner_ros](https://github.com/ivaROS/mbplanner_ros.git) on ROS Noetic.

## Clone the package
```
git clone https://github.com/ivaROS/mbplanner_ws.git
```  

## Setup the workspace
### Ubuntu 20.04 with ROS Noetic:
Use the ```noetic-devel``` branch
```bash
cd mbplanner_ws
git checkout noetic-devel
catkin init
# (any relevant 'catkin config' commands, e.g. -DCMAKE_BUILD_TYPE=Release)
```

For previous versions of ROS, please see the the [upstream repo](https://github.com/unr-arl/mbplanner_ws.git).

### Clone required packages
```bash
wstool init
# https:
wstool merge -t src packages_https.rosinstall
# ssh: use following command to clone using ssh
# wstool merge -t src packages_ssh.rosinstall
wstool update -t src -j 20
```

### Build the whole workspace
```
catkin build
````
