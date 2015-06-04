cmake_minimum_required(VERSION 3.2 FATAL_ERROR)
project(init CXX)

#    Set CMake Install Path
set (CMAKE_INSTALL_PREFIX ${CMAKE_BINARY_DIR} CACHE PATH "default install path" FORCE )

#	CMake module path for custom module finding
set( CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/modules)
set(CMAKE_CXX_FLAGS ${CMAKE_CXX_COMPILER_FLAGS} -std=c++11)

add_subdirectory(src)
add_subdirectory(test)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})
