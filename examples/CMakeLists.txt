project (heightmap_manipulations_examples)
add_executable(save_png save_png.c)

find_package(PNG REQUIRED)
include_directories(${PNG_INCLUDE_DIR})
target_link_libraries(save_png ${PNG_LIBRARY} -lm)

set(CMAKE_C_FLAGS "-std=c99")