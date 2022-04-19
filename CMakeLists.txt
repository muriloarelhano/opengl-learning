cmake_minimum_required(VERSION 3.15)
project(openlgl-learning VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(openlgl-learning "src/main.cpp")

find_package(GLEW REQUIRED)
find_package(glfw3 CONFIG REQUIRED)

target_link_libraries(${PROJECT_NAME} PRIVATE glfw)
target_link_libraries(${PROJECT_NAME} PRIVATE GLEW::GLEW)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
