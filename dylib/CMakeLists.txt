# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)



# 项目信息
project (dyLib)
add_subdirectory(src)
add_subdirectory(test)

add_dependencies(testMain testDyLibrary)



