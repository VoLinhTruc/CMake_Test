# cmake .. -G "MinGW Makefiles"
# set(DCMAKE_GENERATOR "MinGW Makefiles" CACHE STRING "MinGW" FORCE)

cmake_minimum_required(VERSION 3.20.0)
project(MyProject VERSION 1.0.0)

# add_library(hello hello/hello.h hello/hello.cpp)

add_executable(main main.cpp)

target_link_libraries(main libhello.a)