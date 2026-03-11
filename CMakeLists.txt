cmake_minimum_required(VERSION 3.10)
project(StellaEngine)

# 1. Compile Option
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# 2. App
add_executable(StellaEngine ./src/main.cpp)
target_include_directories(StellaEngine PRIVATE src)

# 3. Debug
add_executable(Debug_StellaEngine ./src/ig_run.cpp)
target_include_directories(Debug_StellaEngine PRIVATE src)

# 4. Debug Macro
target_compile_definitions(Debug_StellaEngine PRIVATE DEBUG_MODE)