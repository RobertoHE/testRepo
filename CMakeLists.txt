cmake_minimum_required(VERSION 3.13.0)

PROJECT(test)
#INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})

add_library ("${PROJECT_NAME}" STATIC )

target_sources("${PROJECT_NAME}" PUBLIC test.c test.h)
