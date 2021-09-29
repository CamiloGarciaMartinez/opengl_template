cmake_minimum_required(VERSION 3.5)
project(opengl_project_app VERSION 0.0.1 LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 11)


# add executable
add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME} opengl_project_engine)
target_include_directories(${PROJECT_NAME} PRIVATE opengl_project_engine)