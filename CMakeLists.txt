cmake_minimum_required(VERSION 3.22)
project(SFMLproject)

add_subdirectory(SFML)
include_directories("SFML/include")

project(SFMLproject)

if(WIN32)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /p  ermissive- /W3")
elseif(UNIX)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wpedantic")
endif()

add_executable(SFMLproject src/main.cpp)

target_link_libraries(SFMLproject sfml-graphics sfml-system sfml-window)