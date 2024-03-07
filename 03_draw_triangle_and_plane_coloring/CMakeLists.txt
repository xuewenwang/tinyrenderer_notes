
file(GLOB draw_triangle_and_plane_coloring_srcs ./*.cpp)
add_executable(03_draw_triangle_and_plane_coloring ${draw_triangle_and_plane_coloring_srcs})

add_custom_command(TARGET 03_draw_triangle_and_plane_coloring POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/03_draw_triangle_and_plane_coloring" "../../03_draw_triangle_and_plane_coloring/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 03_draw_triangle_and_plane_coloring/03_draw_triangle_and_plane_coloring"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
