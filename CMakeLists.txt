# cmake file

cmake_minimum_required(VERSION 3.2)

project(example C CXX)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/")

find_package(LLVM REQUIRED CONFIG)

if(LLVM_FOUND)
  list(APPEND CMAKE_MODULE_PATH
    "${CMAKE_CURRENT_SOURCE_DIR}/cmake/llvm-ir-cmake-utils/cmake/")

  include(LLVMIRUtil RESULT_VARIABLE LLVM_IR_UTIL_FOUND)
endif()

set(CMAKE_INSTALL_MESSAGE "LAZY")

#

add_subdirectory(foo)
add_subdirectory(bar)

