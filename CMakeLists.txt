cmake_minimum_required(VERSION 3.5)
project(autoware_world_description_ros2)

find_package(ament_cmake REQUIRED)

install(DIRECTORY worlds
  DESTINATION share/${PROJECT_NAME}/
)

ament_package()
