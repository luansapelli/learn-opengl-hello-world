cmake_minimum_required(VERSION 3.12)
project(learn_opengl)

set(CMAKE_CXX_STANDARD 14)

add_executable(learn_opengl src/main.cpp)

include_directories(dependencies/include)

add_library(glad dependencies/lib/glad.c)
add_library(glfw STATIC IMPORTED)

if (CMAKE_SYSTEM_PROCESSOR MATCHES "arm")
    set_target_properties(glfw PROPERTIES IMPORTED_LOCATION "${CMAKE_CURRENT_SOURCE_DIR}/dependencies/lib/libglfw3_arm.a")
    target_link_libraries(learn_opengl PRIVATE
            "-framework CoreFoundation"
            "-framework Cocoa"
            "-framework IOKit"
            glad
            glfw
    )
else()
    set_target_properties(glfw PROPERTIES IMPORTED_LOCATION "${CMAKE_CURRENT_SOURCE_DIR}/dependencies/lib/libglfw3.a")
    target_link_libraries(learn_opengl glad glfw)
endif()