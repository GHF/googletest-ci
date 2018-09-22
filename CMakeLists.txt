cmake_minimum_required(VERSION 2.8.4)

# Workaround for https://gitlab.kitware.com/cmake/cmake/issues/18198
# TODO: Eventually remove in favor of cmake_minimum_required(VERSION 3.12.1)
cmake_policy(SET CMP0057 NEW)

find_package(GTest REQUIRED)
find_package(Threads REQUIRED)

include_directories(${GTEST_INCLUDE_DIRS})

add_executable(foo_test foo_test.cc)
target_link_libraries(foo_test ${GTEST_BOTH_LIBRARIES})
target_link_libraries(foo_test ${CMAKE_THREAD_LIBS_INIT})

enable_testing()
GTEST_ADD_TESTS(foo_test "" foo_test.cc)
