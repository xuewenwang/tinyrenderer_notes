
file(GLOB zbuffer_srcs ./*.cpp)
add_executable(04zbuffer ${zbuffer_srcs})

add_custom_command(TARGET 04zbuffer POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/04zbuffer" "../../04zbuffer/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 04zbuffer/04zbuffer"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
