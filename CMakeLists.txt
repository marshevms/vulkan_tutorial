cmake_minimum_required(VERSION 3.5)

project(vulkantest LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(vulkantest
main.cpp
queue_family_indices.cpp
)
target_link_libraries(vulkantest Vulkan::Vulkan glfw)
