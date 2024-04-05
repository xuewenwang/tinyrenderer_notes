
file(GLOB Shader_srcs ./*.cpp)
add_executable(07Shader ${Shader_srcs})

if(CMAKE_HOST_WIN32)
    set(SRC_FILE "../bin/07Shader.exe")
else()
    set(SRC_FILE "../bin/07Shader")
endif()

set(DST_DIR "../../07Shader/")

add_custom_command(TARGET 07Shader POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy ${SRC_FILE} ${DST_DIR}
        COMMAND ${CMAKE_COMMAND} -E echo "copy executable target to 07Shader/07Shader"
        COMMAND ${CMAKE_COMMAND} -E echo
        COMMAND ${CMAKE_COMMAND} -E echo
    )
