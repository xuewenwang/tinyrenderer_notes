
file(GLOB zbuffer_srcs ./*.cpp)
add_executable(04zbuffer ${zbuffer_srcs})

if(CMAKE_HOST_WIN32)
    set(SRC_FILE "../bin/04zbuffer.exe")
else()
    set(SRC_FILE "../bin/04zbuffer")
endif()

set(DST_DIR "../../04zbuffer/")


add_custom_command(TARGET 04zbuffer POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${SRC_FILE} ${DST_DIR}
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 04zbuffer/04zbuffer"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
