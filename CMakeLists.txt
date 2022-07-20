# Normal CMakeList
#cmake_minimum_required(VERSION 3.17)
#project(Clion_proj1)
#
#set(CMAKE_CXX_STANDARD 20)
#
#INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)
#link_directories(${PROJECT_SOURCE_DIR}/lib)
#
## add_executable(test1 src/test1.cpp)
#
## target_link_libraries(test1 vulkan-1.lib glfw3.dll)
#
#ADD_DEFINITIONS(-DDEBUG)
#
#add_executable(test2 src/test2.cpp)
#
#target_link_libraries(test2 vulkan-1.lib glfw3.dll)
#

# CMakeList designed for MacOS
cmake_minimum_required(VERSION 3.17)
project(Clion_proj1)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_C_COMPILER "/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc")
set(CMAKE_CXX_COMPILER "/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++")

# glfw
include_directories(/usr/local/Cellar/glfw/3.3.7/include)
link_directories(/usr/local/Cellar/glfw/3.3.7/lib)

# vulkan
include_directories(/Users/s1mplesonny/Code/Tools/Vulkan/macOS/include)
link_libraries(/Users/s1mplesonny/Code/Tools/Vulkan/macOS/lib)

ADD_DEFINITIONS(-DMAC_OS)

find_package(Vulkan REQUIRED FATA_ERROR)
set(librariesList
        GLFW
        Vulkan::Vulkan
        )

add_executable(Clion_proj1 src/test2.cpp)
target_link_libraries(Clion_proj1 ${librariesList})

