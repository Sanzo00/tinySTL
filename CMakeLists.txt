cmake_minimum_required(VERSION 2.8)

project(tinySTL)

include_directories(.)

# version
set(tinySTL_VERSION_MAJOR 0)
set(tinySTL_VERSION_MINOR 1)
set(tinySTL_VERSION_PATCH 0)
set(tinySTL_VERSION "${tinySTL_VERSION_MAJOR}.${tinySTL_VERSION_MINOR}.${tinySTL_VERSION_PATCH}")
message(STATUS "The version of this project is: ${tinySTL_VERSION}")

# build type
set(CMAKE_BUILD_TYPE release)

# gcc 参数
# -Wextra           打印一些额外的警告信息。
# Wno-sign-compare  忽略符号数和无符号数比较的警告信息

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -Wno-sign-compare -Wno-unused-but-set-variable")
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -Wno-sign-compare -Wno-unused-but-set-variable -Wno-array-bound")

# c++11
if (CMAKE_CXX_COMPILER_VERSION VERSION_LESS "5.0.0")
	message(FATAL_ERROR "required GCC 5.0 or later")
else()
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
endif()

message(STATUS "The cmake_cxx_flags is: ${CMAKE_CXX_FLAGS}")

add_subdirectory(test)
