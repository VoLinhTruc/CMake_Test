# cmake .. -G "MinGW Makefiles"
# set(CMAKE_GENERATOR "MinGW Makefiles" CACHE STRING "MinGW" FORCE)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/CMake_Utility)


cmake_minimum_required(VERSION 3.20.0)
project(MyProject VERSION 1.0.0)

# -----------------------------------------------------------------------
# Add include directory
# include_directories(${CMAKE_CURRENT_SOURCE_DIR}/lib_1)

# Add include directory recursive
INC_DIRECTORIES_RECURSIVE(${CMAKE_CURRENT_SOURCE_DIR} all_inc_dir)
include_directories(${all_inc_dir})
# -----------------------------------------------------------------------


# -----------------------------------------------------------------------
# Create static library at specific directory
# set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib_1)
# add_library(hello STATIC ${CMAKE_CURRENT_SOURCE_DIR}/lib_1/hello.cpp)
# -----------------------------------------------------------------------


# -----------------------------------------------------------------------
# Build with dependency
# add_executable(main main.cpp ${CMAKE_CURRENT_SOURCE_DIR}/lib_1/hello.cpp)

# Build with dependency recursively
# set(all_src "")
# file(GLOB_RECURSE all_src_0 "lib_1/*.cpp")
# set(all_src ${all_src} ${all_src_0})
# add_executable(main main.cpp ${all_src})


# Build then link to library
add_executable(main main.cpp)
# Link to library created by this project
# target_link_libraries(main hello)
# Link to outside library
# target_link_libraries(main ${CMAKE_SOURCE_DIR}/lib_1/libhello.a)
# Link to outside library recursively
# set(all_lib "")
# file(GLOB_RECURSE all_lib_0 "lib_1/*.a")
# set(all_lib ${all_lib} ${all_lib_0})
# target_link_libraries(main ${all_lib})
# -----------------------------------------------------------------------
