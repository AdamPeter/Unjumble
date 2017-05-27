
# Google Tests
project( tests )

set(tests_SRCS
    tests.cc
)

find_package(GTest)

include_directories(${GTEST_ROOT}/include)

add_executable(tests ${tests_SRCS})
target_link_libraries(tests GTest::GTest GTest::Main)
#add_dependencies(GTest)
