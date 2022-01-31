cmake_minimum_required(VERSION 3.0.0)
project(glad VERSION 2)

add_library(${PROJECT_NAME} include/glad/gl.h include/KHR/khrplatform.h src/gl.c)
target_include_directories(glad PUBLIC include)