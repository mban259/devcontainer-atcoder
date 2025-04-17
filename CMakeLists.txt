cmake_minimum_required(VERSION 3.10.0)
project(atcoder VERSION 0.1.0 LANGUAGES C CXX)

add_executable(atcoder main.cpp)

target_compile_options(atcoder 
    PUBLIC
    -Wall -Wextra
)

if (CMAKE_BUILD_TYPE STREQUAL "Debug")
    add_compile_options(
        -fsanitize=address,undefined
    )
else()
    add_compile_options(
        -O2 -march=native -mtune=native
    )
endif()

target_compile_features(atcoder PUBLIC cxx_std_23)