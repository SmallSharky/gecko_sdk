
# TODO
# add_library(
#     gecko-hardware-kit-common-drivers
#     STATIC
#
# )


add_library(
    gecko-hardware-kit-common-drivers-retargetio
    OBJECT
    retargetio.c
)

target_link_libraries(gecko-hardware-kit-common-drivers-retargetio PRIVATE gecko-platform-emlib)
