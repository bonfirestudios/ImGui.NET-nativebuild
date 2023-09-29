cmake_minimum_required(VERSION 3.1)

project(cimgui)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} /Zi")
set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} /Zi")
set(CMAKE_SHARED_LINKER_FLAGS_RELEASE "${CMAKE_SHARED_LINKER_FLAGS_RELEASE} /DEBUG")
set(CMAKE_STATIC_LINKER_FLAGS_RELEASE "${CMAKE_STATIC_LINKER_FLAGS_RELEASE} /DEBUG")

include_directories(cimgui)
add_definitions(-DIMNODES_NAMESPACE=imnodes)

add_library(cimgui SHARED 
    cimgui/cimgui.cpp
    cimgui/cimgui_bonfire.cpp
    cimgui/imgui/imgui.cpp
    cimgui/imgui/imgui_draw.cpp
    cimgui/imgui/imgui_demo.cpp
    cimgui/imgui/imgui_widgets.cpp
	cimgui/imgui/imgui_tables.cpp
    cimplot/cimplot.cpp
    cimplot/implot/implot.cpp
    cimplot/implot/implot_demo.cpp
    cimplot/implot/implot_items.cpp
    cimnodes/cimnodes.cpp
    cimnodes/imnodes/imnodes.cpp
    cimguizmo/cimguizmo.cpp
    cimguizmo/ImGuizmo/ImGuizmo.cpp
    cnetimgui/cnetimgui.cpp
    cnetimgui/netImgui/Code/Client/Private/NetImgui_Api.cpp
    cnetimgui/netImgui/Code/Client/Private/NetImgui_NetworkPosix.cpp
    cnetimgui/netImgui/Code/Client/Private/NetImgui_Client.cpp
    cnetimgui/netImgui/Code/Client/Private/NetImgui_CmdPackets_DrawFrame.cpp
    cnetimgui/netImgui/Code/Client/Private/NetImgui_NetworkWin32.cpp)

target_compile_definitions(cimgui PUBLIC IMGUI_DISABLE_OBSOLETE_FUNCTIONS=1)
target_include_directories(cimgui PUBLIC cimgui/imgui cnetimgui/netImgui/Code/Client)
set_target_properties(cimgui PROPERTIES PREFIX "")