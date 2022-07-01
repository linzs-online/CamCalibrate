cmake_minimum_required( VERSION 2.8 )
project( camCalibrate )

set( CMAKE_CXX_FLAGS "-std=c++11" )

# 寻找OpenCV库
find_package(Opencv REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( camCalibrate camCalibrate.cpp )
target_link_libraries( camCalibrate ${OpenCV_LIBS} )