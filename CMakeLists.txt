cmake_minimum_required(VERSION 3.16)
project(mywin32 VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


set(CMAKE_PREFIX_PATH  "${CMAKE_PREFIX_PATH};c:/Qt/6.5.2/msvc2019_64;c:/opencv")

add_executable( ${CMAKE_PROJECT_NAME}
                WIN32
                hellowin.cpp
)

target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )

target_link_libraries(${CMAKE_PROJECT_NAME} user32.lib gdi32.lib comdlg32.lib advapi32.lib ) 



