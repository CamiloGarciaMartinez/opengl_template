cmake_minimum_required(VERSION 3.5)
project(glad VERSION 0.0.1 LANGUAGES CXX C)
set(CMAKE_CXX_STANDAR 11)

add_library(${PROJECT_NAME} src/glad.c)

target_include_directories(${PROJECT_NAME}
  PUBLIC
    $<INSTALL_INTERFACE::include>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    
  PRIVATE
    include
)

target_link_libraries(${PROJECT_NAME}
  PUBLIC

  PRIVATE
    
)
