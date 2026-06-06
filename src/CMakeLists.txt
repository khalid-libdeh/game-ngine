add_library(engine
    core/Engine.cpp
    platform/Window.cpp
    renderer/Renderer.cpp
    utils/Logger.cpp
)

target_include_directories(engine PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/core
    ${CMAKE_CURRENT_SOURCE_DIR}/platform
    ${CMAKE_CURRENT_SOURCE_DIR}/renderer
    ${CMAKE_CURRENT_SOURCE_DIR}/utils
    ${CMAKE_CURRENT_SOURCE_DIR}/math
)

add_executable(GameApp main.cpp)
target_link_libraries(GameApp PRIVATE engine)