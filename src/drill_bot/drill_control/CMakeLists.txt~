cmake_minimum_required(VERSION 2.8.3)
project(drill_control)

## end effector taking drilling part
# copyright by Luan Doan 
# email: luandoan263@gmail.com
# url repository: https://github.com/luandoan/husky
# CMS Lab, Virginia Tech - June 2016

find_package(catkin REQUIRED COMPONENTS
  roslaunch
)

catkin_package()

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)

roslaunch_add_file_check(launch)

catkin_install_python(PROGRAMS scripts/reset_drill DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY config launch scripts
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)



