# Core library of the unjumbler

project(unjumble C CXX)

set(unjumble_SRCS
    unjumble.cc
)

# Add headers
include_directories(unjumble ${HEADER_LOCATION}/core)


# create the main executable
add_executable(unjumble ${unjumble_SRCS})

add_dependencies(unjumble core)
target_link_libraries(unjumble core)

