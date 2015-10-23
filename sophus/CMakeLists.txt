cmake_minimum_required(VERSION 2.8.3)
project(sophus)
include(ExternalProject)

find_package(catkin REQUIRED)

ExternalProject_Add(
  sophus
  PREFIX ""
  GIT_REPOSITORY git://github.com/strasdat/Sophus.git
  INSTALL_DIR ${CATKIN_DEVEL_PREFIX}
  CMAKE_ARGS -DCMAKE_INSTALL_PREFIX=${CATKIN_DEVEL_PREFIX}
  )

catkin_package(
  )
