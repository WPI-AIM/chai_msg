cmake_minimum_required(VERSION 2.8.3)
project(chai_msg)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
  geometry_msgs
)

 add_message_files(
   FILES
   ObjectState.msg
 )
  generate_messages(
   DEPENDENCIES
   geometry_msgs
   std_msgs
 )
 catkin_package(
  CATKIN_DEPENDS message_runtime
  )

include_directories(
  ${catkin_INCLUDE_DIRS}
)

