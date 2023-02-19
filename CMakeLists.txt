cmake_minimum_required(VERSION 3.17)
project(Clion_proj1)

set(CMAKE_CXX_STANDARD 20)

INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)
link_directories(${PROJECT_SOURCE_DIR}/lib)

# add_executable(test1 src/test1.cpp)

# target_link_libraries(test1 vulkan-1.lib glfw3.dll)

ADD_DEFINITIONS(-DDEBUG)

add_executable(test2 src/test2.cpp)

target_link_libraries(test2 vulkan-1.lib glfw3.dll)

add_executable(test3 src/test3.cpp)

target_link_libraries(test3 vulkan-1.lib glfw3.dll)

add_executable(test4 src/test4.cpp)

target_link_libraries(test4 vulkan-1.lib glfw3.dll)

add_executable(test-devicegroup src/test-devicegroup.cpp)

target_link_libraries(test-devicegroup vulkan-1.lib glfw3.dll)

add_executable(test-devicegroup2 src/test-devicegroup2.cpp)

target_link_libraries(test-devicegroup2 vulkan-1.lib glfw3.dll)