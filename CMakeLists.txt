cmake_minimum_required(VERSION 2.8)
project(bsplinefitting)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

add_definitions(-std=c++11)

cs_add_library(${PROJECT_NAME}
  src/cubic_b_spline.cpp
  src/spline_curve_fitting.cpp
  src/open_cubic_b_spline.cpp
)
target_link_libraries(${PROJECT_NAME})

cs_install()
cs_export()
