cmake_minimum_required(VERSION 3.2)

project(poco-example)

find_package(Poco REQUIRED Foundation)

add_executable(pexa main.cpp)
target_link_libraries(pexa Poco::Foundation)
