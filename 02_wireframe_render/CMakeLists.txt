
file(GLOB wireframe_render_srcs ./*.cpp)
add_executable(02_wireframe_render ${wireframe_render_srcs})

message(STATUS "CMAKE_BINARY_DIR=${CMAKE_BINARY_DIR}")

if(CMAKE_HOST_WIN32)
    set(SRC_FILE "../bin/02_wireframe_render.exe")
else()
    set(SRC_FILE "../bin/02_wireframe_render")
endif()

set(DST_DIR "../../02_wireframe_render/")

add_custom_command(TARGET 02_wireframe_render POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${SRC_FILE} ${DST_DIR}
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 02_wireframe_render/02_wireframe_render"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )

