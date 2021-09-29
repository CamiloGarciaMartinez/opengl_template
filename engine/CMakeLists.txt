cmake_minimum_required(VERSION 3.5)
project(opengl_project_engine VERSION 0.0.1 LANGUAGES CXX C)
set(CMAKE_CXX_STANDAR 11)

# set paths
set(LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}/lib)


# add external libraries
add_subdirectory(${LIB_DIR}/glfw)
add_subdirectory(${LIB_DIR}/glad)

add_library(${PROJECT_NAME} src/engine.cpp)

target_include_directories(${PROJECT_NAME}
  PUBLIC
    $<INSTALL_INTERFACE::include>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  PRIVATE
    glfw
    glad
)

target_link_libraries(${PROJECT_NAME}
  PUBLIC

  PRIVATE
    glfw
    glad
)