cmake_minimum_required(VERSION 2.8.3)
project(iai_pepper_server_msgs)

find_package(catkin REQUIRED COMPONENTS
    message_generation geometry_msgs)
    
add_service_files(DIRECTORY srv
  FILES
  PepperSay.srv
  PepperAnimate.srv
  PepperPointAndSay.srv
  PepperShowAndSay.srv)
 
generate_messages(
  DEPENDENCIES
    geometry_msgs)

catkin_package(
  CATKIN_DEPENDS geometry_msgs)