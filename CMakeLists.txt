cmake_minimum_required(VERSION 2.8.4)

find_package(GTest REQUIRED)
find_package(Threads REQUIRED)

include_directories(${GTEST_INCLUDE_DIRS})

add_executable(foo_test foo_test.cc)
target_link_libraries(foo_test ${GTEST_BOTH_LIBRARIES})
target_link_libraries(foo_test ${CMAKE_THREAD_LIBS_INIT})

enable_testing()
add_test(A foo_test)
