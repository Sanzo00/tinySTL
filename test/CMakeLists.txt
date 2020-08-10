include_directories(${PROJECT_SOURCE_DIR}/tinySTL)
include_directories(${PROJECT_SOURCE_DIR}/tinySTL/allocator)
set(STL_TEST stl_test.cpp)
add_executable(stl_test ${STL_TEST})

#set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/test)
