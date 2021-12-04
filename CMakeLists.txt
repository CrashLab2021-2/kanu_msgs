cmake_minimum_required(VERSION 3.0.2)
project(kanu_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
  rospy
  roscpp
)

add_message_files(
  FILES
  motor_msgs.msg
  pid_msgs.msg
)

add_service_files(
  FILES
  dispenser.srv
  door.srv
  tilt.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
# INCLUDE_DIRS include
# LIBRARIES kanu_msgs
# CATKIN_DEPENDS message_generation std_msgs rospy roscpp
# DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
