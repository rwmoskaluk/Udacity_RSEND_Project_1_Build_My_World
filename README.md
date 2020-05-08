# Udacity_RSEND_Project_1_Build_My_World


[image1]: ./Pictures/Perspective.png "Perspective Gazebo World"
[image2]: ./Pictures/Perspective_Model.png "Perspective Gazebo World Model"
[image3]: ./Pictures/Robot.png "Robot Model"
[image4]: ./Pictures/Output_Message.png "Output message when runing Gazebo world"


![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]

### To Run

```
mkdir build/
cd build
cmake ../
make
export GAZEBO_PLUGIN_PATH=${GAZRBO_PLUGIN_PATH}:/home/ryan/Projects/Udacity/Udacity_RSEND_Project_1_Build_My_World/build
gazebo ../world/created_world
```

Note above change the GAZEBO_PLUGIN_PATH to where the build directory path is created locally

### Lessons Learned

Make sure your building is 100% good before saving and exiting as there appears to be no way to change or modify it after leaving the building editor mode.

Saving a world configuration can be done but make sure to specify the save directory to not loose track of where the world was saved too.

When creating the build directory and then compiling the plugins, make sure to correctly export the build directory for the linked libraries along with starting gazebo from this directory, otherwise an error (see below) will be thrown for where the .so supporting plugin is located.
```
$gzserver world/created_world --verbose
Gazebo multi-robot simulator, version 9.0.0
Copyright (C) 2012 Open Source Robotics Foundation.
Released under the Apache 2 License.
http://gazebosim.org

[Msg] Waiting for master.
[Msg] Connected to gazebo master @ http://127.0.0.1:11345
[Msg] Publicized address: 192.168.3.162
[Err] [Plugin.hh:180] Failed to load plugin libmyplugin.so: libmyplugin.so: cannot open shared object file: No such file or directory

```