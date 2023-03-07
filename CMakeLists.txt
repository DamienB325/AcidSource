cmake_minimum_required (VERSION 3.0.0)
add_subdirectory
project (main CXX)

SET(CMAKE_EXPORT_COMPILE_COMMANDS 1)
SET(CMAKE_CXX_COMPILER "clang++")
SET(CMAKE_CXX_STANDARD_INCLUDE_DIRECTORIES  ${CMAKE_CXX_IMPLICIT_INCLUDE_DIRECTORIES})
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -O0")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -O0")
#target_compile_features(${TARGET_NAME} main cxx_std_17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")
include_directories(include)
file(GLOB SRC src/*.cpp)


add_executable(main ${SRC})
