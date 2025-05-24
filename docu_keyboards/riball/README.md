#  Riball a Handwired Wireless Keyboard with Num Rum, seperate Shift Key and Trackball

WIP

### Needed Module:
get with `git clone https://github.com/badjeff/zmk-pmw3610-driver`


## ZMK local build command
The `--pristine` flag enforces a clean build regardless of the content in the specified directory.


Right (central)
```bash
 west build --pristine  -d build/riball/right -b nice_nano_v2 -- -DSHIELD=riball_right -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/zmk-pmw3610-driver;/workspaces/zmk-config"
```

Left
```bash
 west build --pristine  -d build/riball/left -b nice_nano_v2 -- -DSHIELD=riball_left -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/zmk-pmw3610-driver;/workspaces/zmk-config"
```

#### Non persistent build - e.g. if just the Keymap changed

```bash
 west build  -d build/riball/right -b nice_nano_v2 -- -DSHIELD=riball_right -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/zmk-pmw3610-driver;/workspaces/zmk-config"
```

Left
```bash
 west build  -d build/riball/left -b nice_nano_v2 -- -DSHIELD=riball_left -DZMK_CONFIG=/workspaces/zmk-localvolume/zmk-config/config  -DZMK_EXTRA_MODULES="/workspaces/zmk-modules/zmk-pmw3610-driver;/workspaces/zmk-config"
```