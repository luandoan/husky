cmake_minimum_required(VERSION 2.8.3)
project(drill_msgs)

## end effector taking drilling part
# copyright by Luan Doan 
# email: luandoan263@gmail.com
# url repository: https://github.com/luandoan/husky
# CMS Lab, Virginia Tech - June 2016

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

add_message_files(
  FILES
  DrillStatus.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)

###########
## Build ##
###########


include_directories(
  ${catkin_INCLUDE_DIRS}
)


