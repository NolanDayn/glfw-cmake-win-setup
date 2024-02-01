cmake_minimum_required(VERSION 3.9.1)

project(helloGLFW)
set(CMAKE_CXX_STANDARD 14)

add_executable(helloGLFW "${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/src/glad.c")

target_include_directories(helloGLFW PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/include")
target_link_directories(helloGLFW PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/lib")
TARGET_LINK_LIBRARIES(helloGLFW glfw3dll)

set(EXECUTABLE_OUTPUT_PATH "${CMAKE_CURRENT_SOURCE_DIR}/out")

