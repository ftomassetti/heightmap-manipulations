cmake_minimum_required(VERSION 2.8.4)
project(heightmap_manipulations)

#include_directories("src")

set(SOURCE_FILES lib/heightmap.c)
add_library(heightmap_manip ${SOURCE_FILES})

find_package(PNG REQUIRED)
include_directories(${PNG_INCLUDE_DIR})
target_link_libraries(heightmap_manip ${PNG_LIBRARY})

set(CMAKE_C_FLAGS "-std=c99")

option(WITH_EXAMPLE "compile also the example" ON)

#add_subdirectory (test)
#IF(WITH_EXAMPLE)
	add_subdirectory (examples)
#ENDIF(WITH_EXAMPLE)