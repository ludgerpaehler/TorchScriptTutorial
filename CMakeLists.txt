cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(resnet_test)

find_package(Torch REQUIRED)

add_executable(resnet18 resnet18.cpp)
target_link_libraries(resnet18 "${TORCH_LIBRARIES}")
set_property(TARGET resnet18 PROPERTY CXX_STANDARD 14)
