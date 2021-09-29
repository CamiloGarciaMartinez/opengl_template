cmake_minimum_required(VERSION 3.5)
project(opengl_project_engine VERSION 0.0.1 LANGUAGES CXX)
set(CMAKE_CXX_STANDAR 11)

# add external libraries
add_subdirectory(lib/glfw)

add_library(${PROJECT_NAME} src/engine.cpp)

target_include_directories(${PROJECT_NAME}
  PUBLIC
    $<INSTALL_INTERFACE::include>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  PRIVATE
    glfw
)

target_link_libraries(${PROJECT_NAME}
  PUBLIC

  PRIVATE
    glfw
)