cmake_minimum_required(VERSION 3.5) 
project(HELLO) 

#add_library(libhello SHARED hello.c) 
add_library(libhello STATIC hello.c) 

set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello") 
add_executable(hello main.c) 
target_link_libraries(hello libhello)