cmake_minimum_required(VERSION 3.5)

project(GameEngine LANGUAGES CXX)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_subdirectory(libs/glfw)
find_package(OpenGL REQUIRED)

add_executable(GameEngine src/main.cpp)
target_link_libraries(GameEngine OpenGL::GL glfw)