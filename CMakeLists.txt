cmake_minimum_required(VERSION 3.0.0)
project(atcoder)

include(CTest)
enable_testing()

add_executable(atcoder main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "-Wall -Wextra -O2 -march=native -mtune=native -DEVAL -I/opt/boost/gcc/include -L/opt/boost/gcc/lib")
set(CMAKE_CXX_FLAGS_DEBUG "-fsanitize=address,undefined")
include(CPack)
