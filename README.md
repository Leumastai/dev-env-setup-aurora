
## Installation Process on Nobara Linux

#### - ROS2 and RViz2 installation on docker
since there's no official release for ROS2 on Nobara (or any Fedora based distribution), the only options were to install via - docker or - fedora COPR (repository for unofficial fedora software), i decide to use docker.

from docker-hub, i pulled a VNC flavor of ROS2 humble, for easier visualization, using the command below:
```
└─$ docker pull tiryoh/ros2-desktop-vnc:humble
└─$ docker run -it -p 9999:80 --gpus all --name ros2-humbly --security-opt seccomp=unconfined tiryoh/ros2-desktop-vnc:humble 
```

upon a successful execution, i launched `localhost:9999` where a VNC server is running with a GUI interface to execute `ros` and `rviz2` command on terminal. screenshots can be found in the `images/` folder.

#### - Gazebo
gazebo installation was quite straight forward, as i installed it from the nobara-package-manager (recommended way of in installing sofwares). moreover, there's also a gazebo installation within the docker environment, so that can be helpful as well.

> **next step**: connect my local gazebo installation to ros2 installation on docker, this would help make gazebo use efficient resources from my local host and seamless connection with ros.