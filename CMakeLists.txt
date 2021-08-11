cmake_minimum_required(VERSION 3.5)

project(PowerfulClient LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_definitions(-DUNICODE -D_UNICODE)

include_directories(MainFrame)
include_directories(DuiLibHeaders)
file(GLOB_RECURSE SRCS *.cpp *.rc)
file(GLOB_RECURSE HDRS *.h)

add_subdirectory(MainFrame)
add_subdirectory(DuiLibHeaders)
SET(CMAKE_CXX_FLAGS
    "${CMAKE_CXX_FLAGS} \
-std=c++11 -D_REENTRANT /MDd")
link_directories("${CMAKE_SOURCE_DIR}/DuiLibLibs")

add_executable(PowerfulClient WIN32 PowerfulClient.cpp ${SRCS} ${HDRS})
set(CMAKE_BUILD_TYPE "Debug")