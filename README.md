# Udacity_RSEND_Project_1_Build_My_World
Udacity Robotics Software Engineer Nanodegree project 1

### Lessons Learned

Make sure your building is 100% good before saving and exiting as there appears to be no way to change or modify it after leaving the building editor mode.

Saving a world configuration can be done but make sure to specify the save directory to not loose track of where the world was saved too.

When creating the build directory and then compiling the plugins.  Make sure to correctly export the build directory for the linked libraries along with starting gazebo from this directory, otherwise an error will be thrown for where the .so supporting plugin is located.
