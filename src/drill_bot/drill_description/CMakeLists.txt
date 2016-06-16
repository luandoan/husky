cmake_minimum_required(VERSION 2.8.3)
project(drill_description)

find_package(catkin REQUIRED COMPONENTS
  robot_state_publisher
  roslaunch
)

## end effector taking drilling part
# copyright by Luan Doan 
# email: luandoan263@gmail.com
# url repository: https://github.com/luandoan/husky
# CMS Lab, Virginia Tech - June 2016


catkin_package()

###########
## Build ##
###########

catkin_add_env_hooks(drill_description
  SHELLS sh DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/env-hooks
)

roslaunch_add_file_check(launch)

install(
  DIRECTORY launch meshes urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)


