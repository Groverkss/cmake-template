cmake_minimum_required(VERSION 3.12)

project(project_name  VERSION 1.0
                      DESCRIPTION "Project description"
                      LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14 CACHE STRING "C++ standard to conform to")
set(CMAKE_CXX_STANDARD_REQUIRED)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "Create indexing for clangd")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Compile DEBUG builds with debug flags.
set(CMAKE_CXX_FLAGS_DEBUG_INIT "-Wall -g")

# Compile RELEASE builds with optimization flags.
set(CMAKE_CXX_FLAGS_RELEASE_INIT "-O3")

add_subdirectory(lib)

add_subdirectory(src)
