
file(GLOB move_view_angle_srcs ./*.cpp)
add_executable(06_move_view_angle ${move_view_angle_srcs})

add_custom_command(TARGET 06_move_view_angle POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/06_move_view_angle" "../../06_move_view_angle/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 06_move_view_angle/06_move_view_angle"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
