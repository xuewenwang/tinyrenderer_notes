
file(GLOB Shader_srcs ./*.cpp)
add_executable(07Shader ${Shader_srcs})

add_custom_command(TARGET 07Shader POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy "../bin/07Shader" "../../07Shader/"
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 07Shader/07Shader"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
