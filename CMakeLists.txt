cmake_minimum_required(VERSION 3.5)
project(gazebo_world_description)

find_package(ament_cmake REQUIRED)

install(CODE "execute_process( \
  COMMAND  cp -rL \
  ${CMAKE_CURRENT_SOURCE_DIR}/worlds/ \
  ${CMAKE_INSTALL_PREFIX}/${CATKIN_PACKAGE_SHARE_DESTINATION}/)"
)

install(CODE "execute_process( \
  COMMAND  cp -rL \
  ${CMAKE_CURRENT_SOURCE_DIR}/models/ \
  ${CMAKE_INSTALL_PREFIX}/${CATKIN_PACKAGE_SHARE_DESTINATION}/)"
)

ament_package()
