cmake_minimum_required(VERSION 3.10)
project(SFTransperent LANGUAGES CXX)
set(CMAKE_CXX_STANDARD 23)

find_package(SFML 3 COMPONENTS Graphics Window System REQUIRED GLOBAL)

add_library(SFTransperent STATIC src/RWindow.cpp)
target_include_directories(SFTransperent PUBLIC include)
target_link_libraries(SFTransperent PUBLIC SFML::Graphics SFML::Window SFML::System)