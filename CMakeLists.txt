# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Initialise pico_sdk from installed location
# (note this can come from environment, CMake cache etc)
set(PICO_SDK_PATH "/Users/igalieri/working-copy/microcontroller/pico-sdk")

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(pico-display-nn C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(pico-display-nn pico-display-nn.c )

pico_set_program_name(pico-display-nn "pico-display-nn")
pico_set_program_version(pico-display-nn "0.1")

pico_enable_stdio_uart(pico-display-nn 0)
pico_enable_stdio_usb(pico-display-nn 1)

# Add the standard library to the build
target_link_libraries(pico-display-nn pico_stdlib)

pico_add_extra_outputs(pico-display-nn)

