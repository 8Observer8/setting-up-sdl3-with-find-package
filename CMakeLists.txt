cmake_minimum_required(VERSION 3.20)

project(setting-up-sdl3-with-find-package)
add_executable(app)

target_sources(app
PRIVATE
    src/main.cpp
)

find_package(SDL3)
target_link_libraries(app PRIVATE SDL3::SDL3)
target_link_options(app PRIVATE -static)
