cmake_minimum_required(VERSION 3.10)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(PROJECT_NAME "ImGuiColorTextEdit")

project(${PROJECT_NAME} CXX)

set(SOURCES
    "TextEditor.h"
    "TextEditor.cpp"
)

add_library(${PROJECT_NAME} STATIC
    ${SOURCES}
)

target_link_libraries(${PROJECT_NAME}
    imgui
)

target_include_directories(${PROJECT_NAME}
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}"
)

EASE_configure_library_Apple(${PROJECT_NAME} "")

