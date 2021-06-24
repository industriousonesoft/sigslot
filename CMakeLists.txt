cmake_minimum_required(VERSION 3.8)

project(sigslot VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set (LIB_SOURCES 
    src/sigslot.cc
)

set (LIB_HEADERS 
    include/sigslot.h
)

add_library(sigslot STATIC ${LIB_SOURCES} ${LIB_HEADERS})

set_target_properties(sigslot PROPERTIES VERSION ${PROJECT_VERSION} CXX_STANDARD 17)

target_include_directories(sigslot PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)