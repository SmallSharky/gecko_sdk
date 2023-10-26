

add_library(
    gecko-util-thirdparty-segger
    STATIC
    systemview/SEGGER/SEGGER_RTT.c
    systemview/SEGGER/SEGGER_RTT_printf.c
    systemview/SEGGER/SEGGER_SYSVIEW.c
    systemview/init/SEGGER_SYSVIEW_Init.c
    )
