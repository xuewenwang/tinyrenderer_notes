
file(GLOB move_view_angle_srcs ./*.cpp)
add_executable(06_move_view_angle ${move_view_angle_srcs})

if(CMAKE_HOST_WIN32)
    set(SRC_FILE "../bin/06_move_view_angle.exe")
else()
    set(SRC_FILE "../bin/06_move_view_angle")
endif()

set(DST_DIR "../../06_move_view_angle/")

add_custom_command(TARGET 06_move_view_angle POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${SRC_FILE} ${DST_DIR}
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 06_move_view_angle/06_move_view_angle"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
