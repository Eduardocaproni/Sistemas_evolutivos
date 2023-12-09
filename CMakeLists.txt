cmake_minimum_required(VERSION 3.10)
project(MyProject)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 11)

# Specify the source file for your code
set(SOURCE_FILES main.cpp)

# Specify the paths to Eigen and MiniDNN
set(EIGEN_INCLUDE_DIR lib//eigen)
set(MINIDNN_INCLUDE_DIR lib//MiniDNN//include)

# Add the include directories
include_directories(${EIGEN_INCLUDE_DIR} ${MINIDNN_INCLUDE_DIR})

# Add executable target
add_executable(my_executable ${SOURCE_FILES})

# Set optimization level
target_compile_options(my_executable PRIVATE)