# CMakeLists for a shared library

cmake_minimum_required(VERSION 3.2)
project(shared_lib)

set(HEADER_FILES greeter.h) # Set your header files here
set(SOURCE_FILES greeter.cpp) # Set your source files here

add_library(shared_lib SHARED STATIC ${SOURCE_FILES} ${HEADER_FILES})
install(TARGETS shared_lib DESTINATION ${INSTALL_LIB_DIR})
install(FILES ${HEADER_FILES} DESTINATION ${INSTALL_INCLUDE_DIR})