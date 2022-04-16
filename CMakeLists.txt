cmake_minimum_required(VERSION 3.0.0)
project(openlgl-learning VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(openlgl-learning "src/main.cpp")

find_package(GLEW REQUIRED)
target_link_libraries(main PRIVATE GLEW::GLEW)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(main PRIVATE glfw)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
