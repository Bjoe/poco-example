cmake_minimum_required(VERSION 3.11)

project(poco-example)

find_package(Poco CONFIG COMPONENTS Foundation)
if(NOT Poco_FOUND)
  include(FetchContent)
  FetchContent_Declare(
      Poco
      GIT_REPOSITORY https://github.com/pocoproject/poco.git
      GIT_TAG        poco-1.10.1-release
    )
  FetchContent_MakeAvailable(Poco)
endif()

add_executable(pexa main.cpp)
target_link_libraries(pexa Poco::Foundation)
