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

