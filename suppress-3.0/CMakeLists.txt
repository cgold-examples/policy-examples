cmake_minimum_required(VERSION 3.0)
project(foo)

cmake_policy(SET CMP0038 OLD)

add_library(foo foo.cpp)

target_link_libraries(foo foo) # BAD CODE! Make no sense
