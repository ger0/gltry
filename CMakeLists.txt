cmake_minimum_required(VERSION 3.7)

project(gltry)

set(CMAKE_CXX_STANDARD 17)
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)


add_executable(gltry src/main.cpp src/shaderprogram.cpp)
target_link_libraries(gltry glfw)
target_link_libraries(gltry GLEW::GLEW)
target_link_libraries(gltry GL) 
