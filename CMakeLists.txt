cmake_minimum_required(VERSION 3.28)
project(graphics_renderer)

set(CMAKE_CXX_STANDARD 17)

find_package(Vulkan REQUIRED)

include_directories(${Vulkan_INCLUDE_DIRS})
include_directories("/usr/local/include")

add_executable(graphics_renderer main.cpp
)

target_link_libraries(graphics_renderer Vulkan::Vulkan)
target_link_libraries(graphics_renderer "/usr/local/lib/libglfw.3.4.dylib")