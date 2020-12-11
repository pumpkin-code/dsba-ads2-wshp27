include_directories(../src)
include_directories(.)

add_executable(cartestree_tests
    # list of tests
    cartestree_test.cpp

    # list of sources of the lib   
    ../src/cartestree/cartestree.hpp

    # gtest sources
    gtest/gtest-all.cc
    gtest/gtest_main.cc
)

# add pthread for unix systems
if (UNIX)
    target_link_libraries(cartestree_tests pthread)
endif ()
