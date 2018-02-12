cmake_minimum_required (VERSION 2.6)

project (blake2)

file(GLOB SRC
    ref/*.h
    ref/*.c
)

add_library(${PROJECT_NAME} ${SRC})