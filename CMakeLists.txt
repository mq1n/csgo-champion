cmake_minimum_required(VERSION 2.8.4)
project(champion)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -m64 -std=c++11 -Wunused")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -O3 -m64 -std=c++17 -Wall")
set(CMAKE_CXX_FLAGS_MINSIZEREL "${CMAKE_CXX_FLAGS_MINSIZEREL} -std=c++17 -Wall")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ./bin/)

set(CMAKE_BUILD_TYPE RELEASE)

file(GLOB SOURCE_FILES "${CMAKE_SOURCE_DIR}/src/*.cpp")
add_executable(champion ${SOURCE_FILES})
target_link_libraries(champion "-lX11 -lconfig++" xdo)
