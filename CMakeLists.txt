cmake_minimum_required(VERSION 3.12)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(GLFW_ImGUI_Template)

find_package(OpenGL REQUIRED)

# DEPENDENCIES
add_subdirectory(external)
include_directories(external/)


# CORE
add_executable(GLFW_ImGUI_Template
        src/main.cpp)

target_link_libraries(GLFW_ImGUI_Template PRIVATE glfw OpenGL::GL glad glm imgui)