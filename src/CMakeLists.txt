cmake_minimum_required(VERSION 3.2)

include_directories(${PROJECT_SOURCE_DIR}/src/shared_lib)

add_subdirectory(shared_lib)
add_subdirectory(executable)