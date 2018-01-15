PROJECT(MyHello)
cmake_minimum_required(VERSION 3.0)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)

CONAN_BASIC_SETUP()

include ("share/llvm/cmake/LLVMConfig")
include ("share/clang/cmake/ClangConfig")

IF(NOT LLVM_INSTALL_PREFIX)
    MESSAGE(FATAL_ERROR "ERROR! LLVM NOT FOUND!")
ENDIF()
