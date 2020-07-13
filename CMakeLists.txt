
cmake_minimum_required(VERSION 3.16)
project(lua)

file(GLOB SOURCES "*.c")
list(REMOVE_ITEM SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/lua.c")

set(LUA_INCLUDE_DIRS ${PROJECT_SOURCE_DIR})
set(LUA_LIBRARIES $<TARGET_FILE:lua>)

add_library(lua STATIC ${SOURCES})
