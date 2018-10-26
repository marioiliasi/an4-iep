cmake_minimum_required(VERSION 2.8.9)
project(test)
set(CMAKE_BUILD_TYPE Release)

#Bring the headers, such as testl.h into the project
include_directories(include)

#file(GLOB SOURCES "src/*.cpp")

add_library(testlib STATIC src/test.cpp)
#add_library(testlib SHARED ${SOURCES})

#add_executable(include/testl ${SOURCES})

#install(TARGETS testlib DESTINATION /usr/lib)



