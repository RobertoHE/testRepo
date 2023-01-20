cmake_minimum_required(VERSION 3.0)

PROJECT(test)
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})

add_library (test STATIC )


target_sources(test PUBLIC test.c)
