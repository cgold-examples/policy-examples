cmake_minimum_required(VERSION 2.8)
project(foo)

add_library(foo foo.cpp)

target_link_libraries(foo foo) # BAD CODE! Make no sense
