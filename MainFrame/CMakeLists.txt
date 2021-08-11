set(main_frame_SRCS 
    ControlEx.cpp
    MainWnd.cpp
    MsgWnd.cpp
    PopWnd.cpp
    SkinManager.cpp
    SplashWnd.cpp
    )

set(main_frame_HEADERS
    ControlEx.h
    MainWnd.h
    MsgWnd.h
    PopWnd.h
    resource.h
    SkinFrame.h
    SkinManager.h
    SplashWnd.h
    )

include_directories(${CMAKE_SOURCE_DIR}/DuiLibHeaders)
include_directories(${CMAKE_SOURCE_DIR})
message(STATUS "CMAKE_SOURCE_DIR=${CMAKE_SOURCE_DIR}")