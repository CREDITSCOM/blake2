cmake_minimum_required (VERSION 2.6)

project (blake2)

if (MSVC)
  add_definitions(-D__SSE4_1__)
else()
  SET(GCC_COVERAGE_COMPILE_FLAGS "-msse4.1")
endif()

SET(CMAKE_C_FLAGS  "${CMAKE_C_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS}" )

add_library(blake2
  sse/blake2-impl.h
  sse/blake2.h
  sse/blake2b.c
  sse/blake2bp.c
  sse/blake2s.c
  sse/blake2sp.c
  sse/blake2xb.c
  sse/blake2xs.c )

target_include_directories(blake2 PUBLIC sse)
