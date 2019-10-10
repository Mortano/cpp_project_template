# CMakeLists for an executable

cmake_minimum_required(VERSION 3.2)
project(executable)

set(SOURCE_FILES executable.cpp) # Set your source files here

add_executable(executable ${SOURCE_FILES})
target_link_libraries(executable shared_lib) # Link to shared library, if desired
install(TARGETS executable DESTINATION ${INSTALL_EXECUTABLE_DIR})