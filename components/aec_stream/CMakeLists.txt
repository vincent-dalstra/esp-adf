set(COMPONENT_SRCS "")
set(COMPONENT_ADD_INCLUDEDIRS "include")


set(COMPONENT_REQUIRES audio_pipeline driver audio_sal esp_http_client tcp_transport spiffs audio_board esp-adf-libs bootloader_support esp_dispatcher esp_partition mbedtls)



if((${IDF_TARGET} STREQUAL "esp32") OR (${IDF_TARGET} STREQUAL "esp32s3") OR (${IDF_TARGET} STREQUAL "esp32p4")  OR (${IDF_TARGET} STREQUAL "esp32c5"))
	list(APPEND COMPONENT_SRCS "aec_stream.c")
	list(APPEND COMPONENT_REQUIRES esp-sr)
endif()

register_component()
