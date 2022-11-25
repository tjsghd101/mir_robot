cmake_minimum_required(VERSION 2.8.3)
project(mir_srv)

find_package(catkin REQUIRED COMPONENTS
    std_msgs
    geometry_msgs
    message_generation
)

add_service_files(
    FILES
    ./pose_desired.srv
)

generate_messages(
    DEPENDENCIES
    std_msgs
    geometry_msgs
) 

catkin_package(
    CATKIN_DEPENDS std_msgs message_runtime
)
