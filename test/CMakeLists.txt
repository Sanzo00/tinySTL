include_directories(${PROJECT_SOURCE_DIR}/tinySTL)
set(STL_TEST test.cpp)
#set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/test)
add_executable(stl_test ${STL_TEST})
