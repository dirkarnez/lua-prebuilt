lua-prebuilt
============
Prebuilt of [The Programming Language Lua](https://www.lua.org/) official release on ftp site

### Notes
- the official Makefile is not very Windows-friendly

### TODOs (Probably requires forking Lua)
- [ ] Add CMake Support:
  - Possible `CMakeLists.txt`
    ```CMake
    cmake_minimum_required(VERSION 3.14)

    project(lua)

    file(GLOB LUA_HEADERS include/lua/*.h include/lua/*.hpp)
    file(GLOB LUA_SOURCES src/*.c)

    add_library(lua STATIC ${LUA_SOURCES} ${LUA_HEADERS})

    target_include_directories(lua PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include/lua")
    ```
      - [Apolo/CMakeLists.txt at master · MikeLankamp/Apolo](https://github.com/MikeLankamp/Apolo/blob/master/lib/lua-5.3.5/CMakeLists.txt)
- [ ] While using Lua as static library, `liblua.dll.a` should not be generated
- [ ] Modifying / overwritten official `#define`s for better use on Windows

### Playground
- [dirkarnez/lua-playground](https://github.com/dirkarnez/lua-playground)
