# Adapt the pinned BLE management module's endpoint API names to the
# paired cormoran ZMK fork. Both functions retain ZMK's normal behavior.
if(CONFIG_ZMK_BLE_MANAGEMENT_STUDIO_RPC)
  zephyr_compile_definitions(
    zmk_endpoint_set_preferred_transport=zmk_endpoints_select_transport
    zmk_endpoint_get_preferred_transport=zmk_endpoints_get_preferred_transport
  )
endif()
