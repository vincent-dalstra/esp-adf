set(COMPONENT_SRCS  "tone_stream.c")
set(COMPONENT_ADD_INCLUDEDIRS "include")

set(COMPONENT_REQUIRES audio_pipeline driver audio_sal esp_http_client tcp_transport spiffs audio_board esp-adf-libs bootloader_support esp_dispatcher esp_actions tone_partition mbedtls)

register_component()
