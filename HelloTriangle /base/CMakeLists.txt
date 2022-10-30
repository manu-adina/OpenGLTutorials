cmake_minimum_required(VERSION 3.24.2)
project(HelloTriangle VERSION 1.0)
find_package(glfw3 3.3 REQUIRED)
add_library(Glad ../libs/glad.c)

add_executable(${PROJECT_NAME} HelloTriangle.cpp)
target_include_directories(Glad PUBLIC "/usr/local/include/")
target_link_libraries(${PROJECT_NAME} PUBLIC Glad glfw)
