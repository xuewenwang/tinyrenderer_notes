
file(GLOB perspective_projection_srcs ./*.cpp)
add_executable(05_perspective_projection ${perspective_projection_srcs})

add_custom_command(TARGET 05_perspective_projection POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/05_perspective_projection" "../../05_perspective_projection/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 05_perspective_projection/05_perspective_projection"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
