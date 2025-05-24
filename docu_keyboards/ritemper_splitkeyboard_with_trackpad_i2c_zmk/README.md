# Temper Keyboard with Trackpad
WIP

## ZMK Building Firmware

to include the Trackpad  the zmk module cirque-input-module from petejohanson (https://github.com/petejohanson/cirque-input-module/tree/main) is requiered. To build to firmware, this module must be cloned and called in the build statement see [ritemper_description](../../../docu_keyboards/ritemper_splitkeyboard_with_trackpad_i2c_zmk/ritemper_description.md)

- to clone the module run `git clone https://github.com/petejohanson/cirque-input-module/tree/main` 
- and make the directiry accessible in zmk docker container
- also note that building this firmware with the trackpad requiers the pointers-move-and-scroll https://github.com/zmkfirmware/zmk/pull/2027

### ZMK local build command
adding the `--pristine` flag enforces a clean build regardless of the content in the specified directory.


Right
```bash
west build  -d build_t/right -b nice_nano_v2 -- -DSHIELD=ritemper_right -DZMK_CONFIG=/workspaces/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/cirque-input-module;/workspaces/zmk-config"
```

Left Central 
```bash
west build --pristine  -d build_t/left -b nice_nano_v2 -- -DSHIELD="ritemper_left nice_view_adapter nice_view" -DZMK_CONFIG=/workspaces/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/cirque-input-module;/workspaces/zmk-config"
```
### Needed Module:
get with `git clone https://github.com/petejohanson/cirque-input-module`