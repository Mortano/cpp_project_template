# CMakeLists for tests

cmake_minimum_required(VERSION 3.2)
project(test_runner)

set(SOURCE_FILES test_main.cpp) # Add your test source files here

add_executable(test_runner ${SOURCE_FILES})
target_link_libraries(test_runner shared_lib) # link shared library, if desired
install(TARGETS test_runner DESTINATION ${INSTALL_EXECUTABLE_DIR})