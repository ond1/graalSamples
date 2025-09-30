cmake_minimum_required(VERSION 3.27)

#[[How to build tje SimpleApp with CMake:
mkdir build_dir
cd build_dir
cmake ../
make
./App
]]

project(SimpleApp)

add_executable(App app.cpp)
target_link_libraries(App PUBLIC "${CMAKE_CURRENT_LIST_DIR}/target/GraalSample.dylib")
target_include_directories(App PUBLIC PATHS "${CMAKE_CURRENT_LIST_DIR}/target")