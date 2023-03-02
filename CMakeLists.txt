cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(resnet_test)

find_package(Torch REQUIRED)

add_executable(model_loader model_loader.cpp)
target_link_libraries(model_loader "${TORCH_LIBRARIES}")
set_property(TARGET model_loader PROPERTY CXX_STANDARD 14)
