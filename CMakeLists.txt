cmake_minimum_required(VERSION 3.2)
project(simple_tri)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(build)
include_directories($ENV{CTRULIB}/include)

set(SOURCE_FILES
    build/vshader.psh.h
    build/vshader_shbin.h
    source/3dmath.c
    source/3dmath.h
    source/gpu.c
    source/gpu.h
    source/main.c
    source/vshader.pica)

add_executable(simple_tri ${SOURCE_FILES} ${CTR})