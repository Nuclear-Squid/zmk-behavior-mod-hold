target_include_directories(app PUBLIC include)

if ((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_MOD_HOLD app PRIVATE src/behavior_mod_hold.c)
endif()
