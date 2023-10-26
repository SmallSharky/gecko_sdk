


add_library(
    gecko-platform-common
    STATIC
    src/sl_assert.c
    src/sl_slist.c
    src/sl_status.c
    src/sl_stdio.c
    src/sl_string.c
    # src/sli_cmsis_os2_ext_task_register.c
)
add_library(gecko-platform-common-headers INTERFACE)

target_include_directories(
    gecko-platform-common-headers
    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/inc
    # PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/inc
    # PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/config
)

target_include_directories(gecko-platform-common PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/config)


target_link_libraries(
    gecko-platform-common
    PRIVATE
    gecko-platform-service-headers
    gecko-platform-common-headers
    gecko-platform-service-headers
)
