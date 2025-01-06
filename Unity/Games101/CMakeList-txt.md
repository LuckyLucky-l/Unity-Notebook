# CMakeList.txt

cmake_minimum_required (VERSION 2.8.11)

project (Transformation)

#set(CMAKE_PREFIX_PATH "C:/Program Files/eigen-3.4.0" ${CMAKE_PREFIX_PATH})

#find_package(Eigen3 REQUIRED)

include_directories("C:/Program Files/eigen-3.4.0")

add_executable (Transformation main.cpp)#添加可执行文件

#关于c的整个编译流程
