idf_component_register(SRCS "app_main.c"
                            "cjson/cJSON.c"
                            "mqtt/mqtt.c"
                            "smartcfg/smartcfg.c"
                            "wifi/wifi_ap.c"
                            "wifi/wifi_sta.c"
                            "interface/button.c"
                            "interface/led.c"
                            "web_server/web_server.c"
                            "spiffs/spiffs.c"
                            "fota/fota.c"
                            "mesh/ble_mesh_user.c"
               INCLUDE_DIRS "."
               EMBED_TXTFILES ${project_dir}/certs/git_ota.pem ${project_dir}/html/webserver.html)
target_compile_options(${COMPONENT_LIB} PRIVATE "-Wno-format")
