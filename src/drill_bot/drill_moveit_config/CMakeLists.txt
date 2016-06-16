cmake_minimum_required(VERSION 2.8.3)
project(drill_moveit_config)

## end effector taking drilling part
# copyright by Luan Doan 
# email: luandoan263@gmail.com
# url repository: https://github.com/luandoan/husky
# CMS Lab, Virginia Tech - June 2016

find_package(catkin REQUIRED COMPONENTS
  roslaunch
)


catkin_package()


include_directories( ${catkin_INCLUDE_DIRS} )

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})


