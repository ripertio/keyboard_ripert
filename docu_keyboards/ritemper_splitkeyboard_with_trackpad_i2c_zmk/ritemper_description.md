# Temper Keyboard with Trackpad


## ZMK Building Firmware

to include the Trackpad  the zmk module cirque-input-module from petejohanson (https://github.com/petejohanson/cirque-input-module/tree/main) is requiered. To build to firmware, this module must be cloned and called in the build statement see [ritemper_description](../../../docu_keyboards/ritemper_splitkeyboard_with_trackpad_i2c_zmk/ritemper_description.md)

- to clone the module run `git clone https://github.com/petejohanson/cirque-input-module/tree/main` 
- and make the directiry accessible in zmk docker container