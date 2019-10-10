cmake_minimum_required(VERSION 3.2)

include("cmake/HunterGate.cmake")

HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.23.103.tar.gz"
    SHA1 "0b8c31bfdf0fd2fa87b4f743aabcd73904afa256"
)

project(cpp_project_template)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -O3")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(INSTALL_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)
set(INSTALL_LIB_DIR ${PROJECT_SOURCE_DIR}/lib/${CMAKE_BUILD_TYPE})
set(INSTALL_EXECUTABLE_DIR ${PROJECT_SOURCE_DIR}/bin/${CMAKE_BUILD_TYPE})

add_subdirectory(src)
add_subdirectory(test)