cmake_minimum_required(VERSION 2.8.9)
project(iep)
set(CMAKE_BUILD_TYPE Release)

#Bring the headers, such as Student.h into the project
add_subdirectory(test)
include_directories(include)
include_directories(test/include)

#Can manually add the sources using the set command as follows:
set(SOURCES src/main.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
#file(GLOB SOURCES "src/*.cpp")

#add_library(testlib STATIC ${SOURCES})

#target_link_libraries(test testlib)

add_executable(testStudent ${SOURCES})
target_link_libraries(testStudent testlib)

#install(TARGETS testStudent DESTINATION /usr/lib)



