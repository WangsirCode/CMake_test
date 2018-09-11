# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目信息
project (StaticLib)

file(GLOB_RECURSE All_SOURCES  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp ${CMAKE_CURRENT_SOURCE_DIR}/*.h)

add_executable(testMain ${All_SOURCES})

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../src)

IF (WIN32)
	target_link_libraries(testMain ${CMAKE_CURRENT_SOURCE_DIR}/../src/Debug/testStaticLibrary.lib)
	MESSAGE(STATUS "Now is windows")
ELSEIF (APPLE)
    target_link_libraries(testMain ${CMAKE_CURRENT_SOURCE_DIR}/../src/Debug/libtestStaticLibrary.a)
	MESSAGE(STATUS "Now is Apple systens.")
ELSEIF (UNIX)
	MESSAGE(STATUS "Now is UNIX-like OS's. Including aPPLE os x  and CygWin")
ENDIF(WIN32)



