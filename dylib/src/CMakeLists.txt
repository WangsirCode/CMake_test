# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目信息
project (dyLib)

file(GLOB_RECURSE All_SOURCES  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/*.h)

add_library(testDyLibrary SHARED ${All_SOURCES})

include_directories(${CMAKE_CURRENT_SOURCE_DIR})