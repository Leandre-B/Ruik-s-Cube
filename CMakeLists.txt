cmake_minimum_required(VERSION 4.0)
project(rubiks LANGUAGES CXX)

if(CMAKE_CXX_COMPILER_ID MATCHES "GNU")
	add_compile_options(-Wall -Wpedantic)
endif()

find_package(SFML 3 REQUIRED COMPONENTS Graphics Audio Network)

add_executable(rubiks 
	src/main.cpp
)
target_link_libraries(rubiks PRIVATE SFML::Graphics SFML::Audio SFML::Network)
target_compile_features(rubiks PRIVATE cxx_std_17)
