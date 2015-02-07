cmake_minimum_required(VERSION 2.8.4)
project(heightmap_manipulations)

#include_directories("src")

set(SOURCE_FILES lib/heightmap.c)
add_library(heightmap_manip ${SOURCE_FILES})

set(CMAKE_C_FLAGS "-std=c99")

option(WITH_EXAMPLE "compile also the example" OFF)

#add_subdirectory (test)
IF(WITH_EXAMPLE)
#	add_subdirectory (examples)
ENDIF(WITH_EXAMPLE)