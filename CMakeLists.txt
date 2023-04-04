cmake_minimum_required(VERSION 3.17)
project(Clion_proj1)

set(CMAKE_CXX_STANDARD 20)

ADD_DEFINITIONS(-DDEBUG)

add_executable(test2 src/test2.cpp)

target_link_libraries(test2 glfw vulkan)
