# Required by FetchContent_MakeAvailable
cmake_minimum_required(VERSION 3.14)
project(Foo)

include(FetchContent)
FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        release-1.11.0
)
FetchContent_MakeAvailable(googletest)

set(CMAKE_CXX_STANDARD 11)
set(TEST_NAME ${PROJECT_NAME}_tests)
add_executable(${TEST_NAME} foo_test.cc)
target_link_libraries(${TEST_NAME} gtest_main)

enable_testing()
include(GoogleTest)
gtest_discover_tests(${TEST_NAME})
