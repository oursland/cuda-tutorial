cmake_minimum_required(VERSION 2.8)
project(program1)

include(FindCUDA)

find_package(CUDA REQUIRED)

include_directories(/usr/local/cuda/include)

add_definitions("-std=c++11 -Wall -ggdb -Ofast -fopt-info-optall")
cuda_add_executable(
  program1
  program1.cpp)
