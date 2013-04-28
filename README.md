dynamixel_motor
===============

ROS Dynamixel nodes. This is catkinized version of dynamixel_motor

* forked from: https://code.google.com/p/ua-ros-pkg/
* more documents: http://ros.org/wiki/dynamixel_motor

difference from original
-----------------------------
dynamixel_controllers/controller_manager.py uses dynamic load of controllers.
which uses package_path of `controller package` and search for module file.
Package path contains the sources of python module before catkin,
but catkinized packages have python sources in `/opt/ros/groovy/lib/python2.7/dist-packages/PACKAGE_NAME` directory (this is different from the result of rospack find PACKAGE_NAME).
Then catkinized controller_manager must load module file directly not using
`roslib.pakcages.get_pkg_dir`.

Please see the commit 4d055813c0724a82a480ba560e6d8dd3cc93a7b8.
