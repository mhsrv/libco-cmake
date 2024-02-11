cmake_minimum_required(VERSION 3.22)
project(co LANGUAGES C)

set(CMAKE_C_STANDARD 90)
set(CMAKE_C_EXTENSIONS OFF)
set(CMAKE_C_STANDARD_REQUIRED TRUE)

add_library(co STATIC libco.h libco.c)
target_compile_options(co PUBLIC "-fomit-frame-pointer")
target_include_directories(co PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")
