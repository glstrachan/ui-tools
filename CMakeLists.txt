cmake_minimum_required(VERSION 3.10)

project(ui-tools)

file(GLOB source_file
     "src/*.cc"
)

message(${PROJECT_SOURCE_DIR})

add_executable(ui-tools ${source_file})
target_include_directories(ui-tools PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )

set(CMAKE_CXX_STANDARD 17)