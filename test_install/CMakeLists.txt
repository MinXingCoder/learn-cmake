cmake_minimum_required(VERSION 3.26)
project(learn-cmake LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_INSTALL_PREFIX ${CMAKE_CURRENT_LIST_DIR}/install)
add_subdirectory(src)