# http://ros.org/doc/groovy/api/catkin/html/user_guide/supposed.html
cmake_minimum_required(VERSION 2.8.3)
project(dynamixel_driver)
# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED COMPONENTS rospy diagnostic_msgs)

catkin_python_setup()

catkin_package(
    DEPENDS
    CATKIN_DEPENDS rospy diagnostic_msgs
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(PROGRAMS
  scripts/change_id.py
  scripts/info_dump.py
  scripts/set_servo_config.py
  scripts/set_torque.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
  )