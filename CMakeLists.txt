cmake_minimum_required(VERSION 3.14)
project(engine)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake ${CMAKE_MODULE_PATH})

find_package(icore REQUIRED)

add_library(${PROJECT_NAME} STATIC no_source.cpp)

target_link_libraries(${PROJECT_NAME} PUBLIC icore)

target_include_directories(${PROJECT_NAME} PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
)