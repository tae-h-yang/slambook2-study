# Declare the minimum version of cmake require
cmake_minimum_required(VERSION 2.8)

# Declare a cmake project
project(HelloSLAM)

# 设置编译模式
# set(CMAKE_BUILD_TYPE "Debug")

# Add an executable
# Syntax：add_executable(program_name source_code_name）
add_executable(helloSLAM helloSLAM.cpp)

# Add hello library
add_library(hello libHelloSLAM.cpp)
# Shared library
add_library(hello_shared SHARED libHelloSLAM.cpp)

# Add an executable program to call the function in the hello library
add_executable(useHello useHello.cpp)
# Link the library file to the executable program
target_link_libraries(useHello hello_shared)
