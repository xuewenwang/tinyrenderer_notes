
file(GLOB perspective_projection_srcs ./*.cpp)
add_executable(05_perspective_projection ${perspective_projection_srcs})

if(CMAKE_HOST_WIN32)
    set(SRC_FILE "../bin/05_perspective_projection.exe")
else()
    set(SRC_FILE "../bin/05_perspective_projection")
endif()

set(DST_DIR "../../05_perspective_projection/")

add_custom_command(TARGET 05_perspective_projection POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${SRC_FILE} ${DST_DIR}
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 05_perspective_projection/05_perspective_projection"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
