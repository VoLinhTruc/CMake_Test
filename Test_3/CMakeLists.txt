# cmake .. -G "MinGW Makefiles"
# set(CMAKE_GENERATOR "MinGW Makefiles" CACHE STRING "MinGW" FORCE)

cmake_minimum_required(VERSION 3.20.0)
project(MyProject VERSION 1.0.0)

add_subdirectory(./hello)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/hello)

add_executable(main main.cpp)
target_link_libraries(main hello)