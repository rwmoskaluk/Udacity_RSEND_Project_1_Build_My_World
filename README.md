# Udacity_RSEND_Project_1_Build_My_World


[image1]: ./Pictures/Perspective.png "Perspective Gazebo World"
[image2]: ./Pictures/Perspective_Model.png "Perspective Gazebo World Model"
[image3]: ./Pictures/Robot.png "Robot Model"

### To Run

```
mkdir build/
cd build
cmake ../
make
export GAZEBO_PLUGIN_PATH=${GAZRBO_PLUGIN_PATH}:/home/ryan/Projects/Udacity/Udacity_RSEND_Project_1_Build_My_World/build
gazebo ../world/created_world
```

### Lessons Learned

Make sure your building is 100% good before saving and exiting as there appears to be no way to change or modify it after leaving the building editor mode.

Saving a world configuration can be done but make sure to specify the save directory to not loose track of where the world was saved too.

When creating the build directory and then compiling the plugins.  Make sure to correctly export the build directory for the linked libraries along with starting gazebo from this directory, otherwise an error will be thrown for where the .so supporting plugin is located.
