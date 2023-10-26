


add_library(
    gecko-platform-service
    STATIC
    EXCLUDE_FROM_ALL
    iostream/src/sl_iostream.c
    # iostream/src/sl_iostream_swo.c
    # iostream/src/sl_iostream_uart.c
    # iostream/src/sl_iostream_swo_itm_8.c
    # iostream/src/sl_iostream_retarget_stdio.c
    # iostream/src/sl_iostream_debug.c
    # iostream/src/sl_iostream_vuart.c
    # iostream/src/sl_iostream_eusart.c
    # iostream/src/sl_iostream_stdlib_config.c
    # iostream/src/sl_iostream_stdio.c
    # iostream/src/sl_iostream_leuart.c
    # iostream/src/sl_iostream_rtt.c
    # iostream/src/sl_iostream_usart.c
    # iostream/src/sl_iostream_cpc.c
)

add_library(gecko-platform-service-headers INTERFACE)

target_include_directories(
    gecko-platform-service-headers
    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/iostream/inc
    # PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/iostream/inc
    # PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/iostream/config
)

target_include_directories(gecko-platform-service PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/iostream/config)

target_link_libraries(
    gecko-platform-service
    PRIVATE
    gecko-platform-service-headers
    gecko-platform-common-headers
    gecko-platform-emlib
)



# target_link_libraries(
#     gecko-platform-service
#     PUBLIC
#     gecko-platform-common
#     gecko-platform-emlib
#     gecko-platform-driver
#     gecko-platform-emdrv
# )

# add_library(gecko-platform-service-iostream-config-s0 INTERFACE)
# add_library(gecko-platform-service-iostream-config-s1 INTERFACE)
# add_library(gecko-platform-service-iostream-config-s2 INTERFACE)
