cmake_minimum_required(VERSION 3.10)

project(ui-tools)

file(GLOB source_file
     "src/*.cc"
     "src/*.cpp"
)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
# include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include") 
# include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include") 
include_directories("${CMAKE_CURRENT_SOURCE_DIR}/lib/pthread")

add_executable(ui-tools ${source_file})
target_include_directories(ui-tools PUBLIC
                           "${CMAKE_CURRENT_SOURCE_DIR}/include"
                           )
target_include_directories(ui-tools PUBLIC
                           "${CMAKE_CURRENT_SOURCE_DIR}/lib"
                           )
target_compile_definitions(ui-tools PUBLIC _WIN32)
set(CMAKE_CXX_STANDARD 17)