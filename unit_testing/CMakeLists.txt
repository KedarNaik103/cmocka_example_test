cmake_minimum_required(VERSION 3.18)
project(test-driven-C)
enable_testing()
set(CMAKE_C_FLAGS "-Wall -Werror -Wpedantic -std=c11")
add_subdirectory(src)
add_subdirectory(test)


