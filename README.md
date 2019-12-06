# melodic_coppeliasim_xarm7
This repository contains simulation of xArm7 controlled by ROS Melodic in Vrep 

Build Docker:
```
sudo docker build --force-rm -t coppelia_arm https://github.com/SoftServeSAG/melodic_coppeliasim_xarm7.git\#:docker
```
```
xhost +local:docker
```
```
sudo docker run --net=host -it --name coppelia_arm_dev -e DISPLAY -e LOCAL_USER_ID=$(id -u) -v /tmp/.X11-unix:/tmp/.X11-unix coppelia_arm:latest
```

Terminal1
```
roscore
```
Terminal2
```
sudo docker ps -l
```
```
sudo docker exec -it coppelia_arm_dev bash
```
```
rostopic list
```
```
cd CoppeliaSim_Edu_V4_0_0_Ubuntu18_04
```
```
./coppeliaSim.sh
```
