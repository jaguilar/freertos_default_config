
if (NOT TARGET freertos_config)
  add_library(freertos_config INTERFACE)
  target_include_directories(freertos_config SYSTEM
    INTERFACE
    freertos_config) # The config file directory
    target_compile_options(freertos_config INTERFACE -DPICO_TIME_DEFAULT_ALARM_POOL_DISABLED)
endif()

if (NOT TARGET lwip_config)
  add_library(lwip_config INTERFACE)
  target_include_directories(lwip_config SYSTEM
    INTERFACE
    lwip_config) # The config file directory
endif()