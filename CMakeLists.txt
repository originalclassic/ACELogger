cmake_minimum_required(VERSION 3.28)
project(ACELogger)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Define source and include directories
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)

# Define source files
set(ACELOGGER_SOURCES
        ${SRC_DIR}/ACELogger.cpp
)

# Create the static library
add_library(ACELogger STATIC ${ACELOGGER_SOURCES})

# Specify include directories
target_include_directories(ACELogger PUBLIC
        ${INCLUDE_DIR}
)
