cmake_minimum_required(VERSION 4.2)
project(vm C)

set(CMAKE_C_STANDARD 11)

include_directories(.)

add_executable(vm
        macros.h
        vm.c
        practice.c)
if(MSVC)
    target_compile_options(vm PRIVATE /Zi)
    target_link_options(vm PRIVATE /DEBUG)
endif()