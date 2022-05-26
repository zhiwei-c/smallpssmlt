# Projects Settings
cmake_minimum_required(VERSION 3.10)

project(smallpssmlt_unobfuscated)

if(NOT DEFINED CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 17)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
endif()

if (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
    add_definitions(/wd"6993" /wd"4996" /wd"4819")
    add_compile_options("$<$<C_COMPILER_ID:MSVC>:/utf-8>")
    add_compile_options("$<$<CXX_COMPILER_ID:MSVC>:/utf-8>")
endif()

project(smallpssmlt_unobfuscated LANGUAGES CXX)

add_executable(smallpssmlt_unobfuscated "${CMAKE_CURRENT_SOURCE_DIR}/src/smallpssmlt_unobfuscated.cpp")

set_property(DIRECTORY PROPERTY VS_STARTUP_PROJECT smallpssmlt_unobfuscated)