cmake_minimum_required(VERSION 3.16)
project(MultiplyTest LANGUAGES CXX)

enable_testing()

find_package(GTest REQUIRED)

add_executable(div_test main.cpp)

target_link_libraries(div_test PRIVATE GTest::gtest GTest::gtest_main)

add_test(div_gtest div_test)