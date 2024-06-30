# CMakeLists.txt
cmake_minimum_required(VERSION 3.15)
project(cpp_template)

find_package(grpc CONFIG REQUIRED)

# main target
add_executable(main)
target_sources(main PRIVATE src/main.cpp)
target_link_libraries(main PRIVATE grpc)
set_property(TARGET main PROPERTY CXX_STANDARD 14)

