cmake_minimum_required(VERSION 3.13.0)

project(mylibrary VERSION 1.0.0 LANGUAGES C)

set(MAIN_PROJECT OFF)
if(CMAKE_CURRENT_SOURCE_DIR STREQUAL CMAKE_SOURCE_DIR)
    set(MAIN_PROJECT ON)
endif()

add_library ("${PROJECT_NAME}" STATIC )
#add_library(${PROJECT_NAME}::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

if(MAIN_PROJECT)
else(MAIN_PROJECT)
    target_include_directories(${PROJECT_NAME} INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/>)
endif(MAIN_PROJECT)

target_sources("${PROJECT_NAME}" PUBLIC mytest.c mytest.h)

