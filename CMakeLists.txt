cmake_minimum_required(VERSION 3.16)
project(MultiplyTest LANGUAGES CXX)

enable_testing()

find_package(GTest REQUIRED)
find_package(ZLIB REQUIRED)


add_executable(div_test main.cpp)
add_executable(main2 main2.cpp)

target_link_libraries(div_test PRIVATE GTest::gtest GTest::gtest_main)
target_link_libraries(main2 ZLIB::ZLIB)

add_test(div_gtest div_test)