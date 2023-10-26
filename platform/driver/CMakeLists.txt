

add_library(
    gecko-platform-driver
    STATIC
    EXCLUDE_FROM_ALL
    debug/src/sl_debug_swo.c
)


add_library(
    gecko-platform-driver-headers
    INTERFACE
)


target_include_directories(
    gecko-platform-driver-headers
    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/inc
)

target_link_libraries(
    gecko-platform-driver
    PRIVATE
    gecko-platform-driver-headers
)

# target_link_libraries(
#     gecko-platform-driver-headers
#     PRIVATE
#     gecko-platform-common-headers
#     gecko-platform-emlib
# )


add_library(gecko-driver-debug-config-s0-gg INTERFACE)
target_include_directories(gecko-driver-debug-config-s0-gg INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/config/s0/gg)

add_library(gecko-driver-debug-config-s0-tg INTERFACE)
target_include_directories(gecko-driver-debug-config-s0-tg INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/config/s0/tg)

add_library(gecko-driver-debug-config-s1 INTERFACE)
target_include_directories(gecko-driver-debug-config-s1 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/config/s1)

add_library(gecko-driver-debug-config-s2 INTERFACE)
target_include_directories(gecko-driver-debug-config-s2 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/config/s2)

add_library(gecko-driver-debug-config-s3 INTERFACE)
target_include_directories(gecko-driver-debug-config-s3 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/debug/config/s3)
