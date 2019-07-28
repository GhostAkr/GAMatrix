cmake_minimum_required(VERSION 3.0.0)

set (CMAKE_C_COMPILER_WORKS 1)
set (CMAKE_CXX_COMPILER_WORKS 1)

project(GAMatrix VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(GAMatrix project/src/main.cpp project/include/Matrix.h project/src/Matrix.cpp)

set(EXECUTABLE_OUTPUT_PATH "")

set_target_properties(${PROJECT_NAME} PROPERTIES OUTPUT_NAME "a")

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
