cmake_minimum_required(VERSION 3.16)
project(UnderHouse C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

if(MSVC)
  add_compile_options(/W4 /utf-8)
else()
  add_compile_options(-Wall -Wextra)
endif()

file(GLOB SOURCES CONFIGURE_DEPENDS src/*.c)
add_executable(underhouse ${SOURCES})
