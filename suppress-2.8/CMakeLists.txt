cmake_minimum_required(VERSION 2.8)
project(foo)

if(POLICY CMP0038)
  # Policy CMP0038 introduced since CMake 3.0 so if we want to be compatible
  # with 2.8 (see cmake_minimum_required) we should put 'cmake_policy' under
  # condition.
  cmake_policy(SET CMP0038 OLD)
endif()

add_library(foo foo.cpp)

target_link_libraries(foo foo) # BAD CODE! Make no sense
