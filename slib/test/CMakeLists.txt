# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目信息
project (StaticLib)

file(GLOB_RECURSE All_SOURCES  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/*.h)

add_executable(testMain ${All_SOURCES})

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../src)

target_link_libraries(testMain ${CMAKE_CURRENT_SOURCE_DIR}/../src/Debug/libtestStaticLibrary.a)
