cmake_minimum_required(VERSION 3.10)
project(http_beastie)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Boost REQUIRED COMPONENTS system)
find_package(Threads REQUIRED)

include_directories(include)

file(GLOB SOURCES "src/*.cpp")

add_executable(http_beastie ${SOURCES})

target_link_libraries(http_beastie
    Boost::system
    Threads::Threads
)