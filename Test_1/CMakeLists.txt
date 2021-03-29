set(CMAKE_GENERATOR "MinGW Makefiles" CACHE STRING "" FORCE)

cmake_minimum_required(VERSION 3.20.0)
project(MyProject VERSION 1.0.0)

add_executable(cmake-good main.cpp)