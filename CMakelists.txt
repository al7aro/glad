cmake_minimum_required(VERSION 3.4...3.28 FATAL_ERROR)

project(glad
    LANGUAGES C
)

file(GLOB_RECURSE source_files
    "./src/glad.c"
    "./include/glad/glad.h"
    "./include/KHR/khrplatform.h"
)

add_library(glad
    ${source_files}
)

target_include_directories(glad PRIVATE "./include/KHR")
target_include_directories(glad PUBLIC "./include")
