cmake_minimum_required(VERSION 3.10)
project(HelloWorld)

set(CMAKE_CXX_STANDARD 20)
include(CTest)

add_executable(TestHelloWorld test_main.cpp)

add_executable(HelloWorld main.cpp)

add_test(NAME HelloWorld COMMAND HelloWorld)
