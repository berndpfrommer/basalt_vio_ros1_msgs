cmake_minimum_required(VERSION 3.5)

project(basalt_vio_ros1_msgs)

find_package(catkin REQUIRED COMPONENTS
std_msgs
message_generation)

add_message_files(DIRECTORY
msg
FILES
KeyPointToAffine.msg
ObservationMap.msg
OpticalFlowResult.msg
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)
