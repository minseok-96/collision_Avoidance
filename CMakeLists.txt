cmake_minimum_required(VERSION 2.8.3)
project(scout_CA)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  sensor_msgs
  tf
  nav_msgs
  morai_msgs
  scout_msgs
  ca_msgs
)

catkin_package(
  CATKIN_DEPENDS
  rospy
  std_msgs
  sensor_msgs
  tf
  nav_msgs
  morai_msgs
  scout_msgs
  ca_msgs
)

catkin_install_python(PROGRAMS
  src/scout_CA.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)
