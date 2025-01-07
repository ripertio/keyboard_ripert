#  Skeletyl Keyboard Handwired Wireless and Sondbox for ZMK features

WIP

## ZMK local build command
The `--pristine` flag enforces a clean build regardless of the content in the specified directory.


Right (central)
```bash
west build --pristine -d build/right -b nice_nano_v2 -- -DSHIELD=riskyl_right -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-localvolume/zmk-modules/cirque-input-module;/workspaces/zmk-localvolume/zmk-config"
```

Left
```bash
west build --pristine -d build/left -b nice_nano_v2 -- -DSHIELD=riskyl_left  -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-localvolume/zmk-modules/cirque-input-module;/workspaces/zmk-localvolume/zmk-config"
```
