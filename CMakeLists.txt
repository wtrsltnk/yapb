cmake_minimum_required(VERSION 3.7)

project(yapb)

add_library(yapb SHARED
    include/resource.h
    include/engine/const.h
    include/engine/eiface.h
    include/engine/enginecallback.h
    include/engine/extdll.h
    include/engine/meta_api.h
    include/engine/progdefs.h
    include/engine/util.h
    include/compress.h
    include/core.h
    include/corelib.h
    include/engine.h
    include/globals.h
    include/platform.h
    project/yapb.rc
    source/basecode.cpp
    source/chatlib.cpp
    source/combat.cpp
    source/engine.cpp
    source/globals.cpp
    source/interface.cpp
    source/manager.cpp
    source/navigate.cpp
    source/support.cpp
    source/waypoint.cpp
    )

target_include_directories(yapb
    PRIVATE include
    PRIVATE include/engine
    )

target_link_libraries(yapb ws2_32)
