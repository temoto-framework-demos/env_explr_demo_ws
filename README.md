# env_explr_demo_ws
Source materials for the human-robot collaboration based environment exploration demo

## Dependencies

Normally one would invoke
``` bash
rosdep install --from-paths WORKSPACE --ignore-src --rosdistro=ROSDISTRO
``` 
but realsense2 ros wrapper has problems with that: [see the issue](https://github.com/IntelRealSense/realsense-ros/issues/808)

hence:

PCL
``` bash
sudo apt install libpcl-dev
sudo apt install ros-melodic-pcl-msgs
sudo apt install ros-melodic-tf2-eigen
```

Realsense
``` bash
https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md#installing-the-packages
```
