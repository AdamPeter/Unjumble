# Core library of the unjumbler

project( core C CXX )

set(core_SRCS
    Unjumbler.cc
)

# Add headers
include_directories(core ${HEADER_LOCATION}/core)

# create static library
add_library(core STATIC ${core_SRCS})


