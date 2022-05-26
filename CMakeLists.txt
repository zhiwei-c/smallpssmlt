# Projects Settings
cmake_minimum_required(VERSION 3.10)

project(small_pssmlt)

add_subdirectory(${PROJECT_SOURCE_DIR}/smallpssmlt)
add_subdirectory(${PROJECT_SOURCE_DIR}/smallpssmlt_unobfuscated)

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT smallpssmlt)