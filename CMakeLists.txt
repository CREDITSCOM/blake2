cmake_minimum_required (VERSION 2.6)

project (blake2)

add_library(${PROJECT_NAME}
  ref/blake2-impl.h
  ref/blake2.h
  ref/blake2b-ref.c
  ref/blake2bp-ref.c
  ref/blake2s-ref.c
  ref/blake2sp-ref.c
  ref/blake2xb-ref.c
  ref/blake2xs-ref.c )

target_include_directories(blake2 PUBLIC ref)