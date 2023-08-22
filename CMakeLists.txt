cmake_minimum_required(VERSION 3.0)

project(myServer C)
set(CMAKE_C_STANDARD 99)

add_executable(myServer open62541.c myServer.c)

if(WIN32)
    target_link_libraries(myServer ws2_32 iphlpapi)
endif()
