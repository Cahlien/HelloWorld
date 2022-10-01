cmake_minimum_required(VERSION 3.23)
project(HelloWorld)

set(CMAKE_CXX_STANDARD 20)
include(CTest)

add_executable(TestHelloWorld test_main.cpp)

add_executable(HelloWorld main.cpp)

add_test(NAME TestHelloWorld COMMAND TestHelloWorld)
