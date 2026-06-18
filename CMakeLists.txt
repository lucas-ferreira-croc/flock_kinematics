cmake_minimum_required(VERSION 3.15)
project(flock_kinematics LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_Library(flock_kinematics SHARED
    src/test.cpp
    src/test.hpp
)

target_include_directories(flock_kinematics PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/src>
)

set_target_properties(flock_kinematics PROPERTIES
    CXX_VISIBILITY_PRESET hidden
    VISIBILITY_INLINES_HIDDEN ON
)

