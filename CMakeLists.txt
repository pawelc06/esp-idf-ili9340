
set(COMPONENT_SRCS
    driver/decode_image.c
    driver/fontx.c
    driver/ili9340.c
    driver/pngle.c
)

set(COMPONENT_ADD_INCLUDEDIRS
    driver/include
)
idf_component_register(SRCS "driver/decode_image.c"  "driver/fontx.c"  "driver/ili9340.c" "driver/pngle.c"
                       INCLUDE_DIRS "driver/include"
                       REQUIRES driver)
    
spiffs_create_partition_image(storage font FLASH_IN_PROJECT)
