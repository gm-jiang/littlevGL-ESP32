set(SOURCES main.c
            connect.c
            usr_sntp.c)

idf_component_register(SRCS ${SOURCES}
                    INCLUDE_DIRS include
                    REQUIRES lvgl_esp32_drivers lvgl_touch lvgl_tft lvgl lv_examples nvs_flash esp_netif lwip)

target_compile_definitions(${COMPONENT_LIB} PRIVATE LV_CONF_INCLUDE_SIMPLE=1)
