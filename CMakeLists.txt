# Required by FetchContent_MakeAvailable
cmake_minimum_required(VERSION 3.14)
project(Foo)

include(FetchContent)
FetchContent_Declare(
  googletest
  GIT_REPOSITORY https://github.com/google/googletest.git
  GIT_TAG        release-1.8.1
)
FetchContent_MakeAvailable(googletest)

add_executable(foo_test foo_test.cc)
target_link_libraries(foo_test gtest_main)
add_test(NAME foo_test COMMAND foo_test.cc)
