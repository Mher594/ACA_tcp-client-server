cmake_minimum_required(VERSION 3.16)

project(client-server LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Boost REQUIRED COMPONENTS system)

add_executable(server server.cpp)
target_link_libraries(server
 PRIVATE
 Boost::system)

 add_executable(client client.cpp)
 target_link_libraries(client
 PRIVATE
 Boost::system)
