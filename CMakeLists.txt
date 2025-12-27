cmake_minimum_required(VERSION 3.12)

project(FastDevFS)

find_package(PkgConfig REQUIRED)
pkg_check_modules(FUSE3 REQUIRED fuse3)

add_executable(FastDevFS main.cpp)
target_include_directories(FastDevFS PRIVATE ${FUSE3_INCLUDE_DIRS})
target_link_libraries(FastDevFS PRIVATE ${FUSE3_LIBRARIES})
target_compile_options(FastDevFS PRIVATE ${FUSE3_CFLAGS_OTHER})