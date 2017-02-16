cmake_minimum_required(VERSION 2.8.3)
project(val_grasping)

find_package(catkin REQUIRED COMPONENTS
  position_controllers
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES val_grasping
#  CATKIN_DEPENDS ros_control ros_controllers
#  DEPENDS system_lib
)

# include_directories(include)
include_directories(
  ${catkin_INCLUDE_DIRS}
)

## Mark other files for installation (e.g. launch and bag files, etc.)
install(DIRECTORY
  config
  launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
