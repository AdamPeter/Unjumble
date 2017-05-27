# Author: Adam Hodgson
message(STATUS "Adam")
# Minimum cmake supported
cmake_minimum_required(VERSION 3.5.0)

# Global project
project(Unjumbler)

set(HEADER_LOCATION ${CMAKE_CURRENT_LIST_DIR}/include)
set(SOURCE_LOCATION ${CMAKE_CURRENT_LIST_DIR}/src)

FILE(GLOB srcs RELATIVE ${SOURCE_LOCATION} ${SOURCE_LOCATION}/*)


# Directories to include in the build
set(Project_DIRS
    tests/
)

message(STATUS "Adding subdirectories")
# Add directories to build
foreach (dir ${srcs})
    add_subdirectory(${SOURCE_LOCATION}/${dir})
endforeach(dir)

foreach (dir ${Project_DIRS})
    add_subdirectory(${dir})
endforeach(dir)




