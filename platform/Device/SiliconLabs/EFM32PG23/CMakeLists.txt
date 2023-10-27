
add_library(
    gecko-device-efm32pg23-headers INTERFACE
)

add_library(
    gecko-device-efm32pg23-nostart
    OBJECT
    Source/system_efm32pg23.c
)


add_library(
    gecko-device-efm32pg23
    OBJECT
    Source/startup_efm32pg23.c
)

target_link_libraries(
    gecko-device-efm32pg23-nostart PUBLIC gecko-device-efm32pg23-headers
)

target_link_libraries(gecko-device-efm32pg23 PUBLIC gecko-device-efm32pg23-nostart)

target_include_directories(
    gecko-device-efm32pg23-headers
    INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/Include
)




target_link_libraries(
    gecko-device-efm32pg23-headers
    INTERFACE
    gecko-platform-cmsis
)
