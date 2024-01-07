cmake_minimum_required(VERSION 3.24)
set(CMAKE_COLOR_DIAGNOSTICS ON)

include($ENV{PICO_SDK_PATH}/external/pico_sdk_import.cmake)

# -- set up the project
project(acoustictracker)

pico_sdk_init()

add_executable(ear
    src/ear.c
    )

target_link_libraries(ear pico_stdlib)

# .{map,bin,elf,hex,uf2} outputs
pico_add_extra_outputs(ear)

