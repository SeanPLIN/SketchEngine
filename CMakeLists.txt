cmake_minimum_required(VERSION 3.10.0)

set(SOLUTION_NAME SketchEngine)
set(ENGINE_NAME Sketch)
set(GAME_NAME Game)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

project(${SOLUTION_NAME})

add_subdirectory(${ENGINE_NAME})
add_subdirectory(${GAME_NAME})

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT ${GAME_NAME})
