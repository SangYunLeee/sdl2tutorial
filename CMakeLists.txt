cmake_minimum_required(VERSION 3.0.0)
project(SDL2Tutorial)

find_package(PkgConfig REQUIRED)

pkg_check_modules(SDL2 REQUIRED sdl2)


add_executable(SDL2Tutorial main.cpp)

target_include_directories(SDL2Tutorial PRIVATE ${SDL2_INCLUDE_DIRS} )
target_link_libraries(SDL2Tutorial PRIVATE ${SDL2_LIBRARIES} )