# creat by mengmeng

cmake_minimum_required(VERSION 2.8)

project(learning_to_create_project)

message("\n #### I love China! #### \n")

set(CMAKE_CXX_STANDARD 11)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

find_package(OpenCV REQUIRED)

include_directories(
        ${PROJECT_SOURCE_DIR}/include/
)

add_library(${PROJECT_NAME} SHARED
        src/China.cpp
        src/i.cpp
        src/love.cpp
)

add_executable(i_love_China example/i_love_China.cpp)
target_link_libraries(i_love_China
        ${OpenCV_LIBS}
        ${PROJECT_NAME}
)

