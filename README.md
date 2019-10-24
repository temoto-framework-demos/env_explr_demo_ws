# env_explr_demo_ws
Source materials for the human-robot collaboration based environment exploration demo

## Dependencies

Normally one would invoke
``` bash
rosdep install --from-paths WORKSPACE --ignore-src --rosdistro=ROSDISTRO
``` 
but realsense2 ros wrapper has problems with that: [see the issue](https://github.com/IntelRealSense/realsense-ros/issues/808)

hence:

**PCL**
``` bash
$ sudo apt install libpcl-dev
$ sudo apt install ros-melodic-pcl-msgs
$ sudo apt install ros-melodic-tf2-eigen
```

**Realsense**
``` bash
https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md#installing-the-packages
```

**rtabmap_ros**
``` bash
$ sudo apt install ros-melodic-rtabmap-ros
$ sudo apt install ros-kinetic-imu-filter-madgwick
```

## Setting up remote desktop

### Adroid device preparation
* [Enable developer options](https://developer.android.com/studio/debug/dev-options) on the android device
* Install a VNC viewer app, [such as this](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android&hl=en)

### Operator PC preparation
Install [Android Debug Bridge](https://linuxtechlab.com/install-adb-fastboot-ubuntu/) and a VNC server on the Operator PC
``` bash
$ sudo apt install android-tools-adb android-tools-fastboot
$ sudo apt install x11vnc
```

### Running and viewing the remote desktop via USB

**On Operator PC**
* Start the VNC server: `$ x11vnc`
* Connect the android device to Operator PC via USB
* Forward android device port 5900 to Operator PC port 5900 `$ adb reverse tcp:5900 tcp:5900`

**On the android device**
* Open the VNC viewer app
* Set the connection to 
  * Address: `localhost::5900`
  * Name: `Operator PC`



