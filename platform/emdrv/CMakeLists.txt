


add_library(
    gecko-platform-emdrv
    STATIC EXCLUDE_FROM_ALL
    dmadrv/src/dmactrl.c
    dmadrv/src/dmadrv.c
)

target_include_directories(
    gecko-platform-emdrv
    INTERFACE
    ${CMAKE_CURRENT_SOURCE_DIR}/dmadrv/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/common/inc
    PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/dmadrv/inc
    ${CMAKE_CURRENT_SOURCE_DIR}/common/inc
)


target_link_libraries(
    gecko-platform-emdrv
    PUBLIC
    gecko-platform-emlib
)
