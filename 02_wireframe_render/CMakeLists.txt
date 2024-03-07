
file(GLOB wireframe_render_srcs ./*.cpp)
add_executable(02_wireframe_render ${wireframe_render_srcs})

add_custom_command(TARGET 02_wireframe_render POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/02_wireframe_render" "../../02_wireframe_render/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 02_wireframe_render/02_wireframe_render"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
