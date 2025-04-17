cmake_minimum_required(VERSION 3.10.0)
project(atcoder VERSION 0.1.0 LANGUAGES C CXX)

add_executable(atcoder main.cpp)

set(CMAKE_CXX_FLAGS_DEBUG "-Wall -Wextra -fsanitize=address,undefined")
set(CMAKE_CXX_FLAGS_RELEASE "-Wall -Wextra -O2 -march=native -mtune=native")

target_compile_features(atcoder PUBLIC cxx_std_23)