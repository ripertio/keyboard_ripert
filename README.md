## Collection of my Keyboard adapation, including ZMK (wirelese) Firmware

WIP

To build the firmware locally, use the following command to create the volume:

```bash
docker volume create --driver local -o o=bind -o type=none \
  -o device="/home/zmk_keyboards/zmk-config" zmk-localvolume
```

If the folder you want to access in Docker is located at i.e. `/home/zmk_keyboards/zmk-config`, make the volume accessible in the ZMK container by editing the cloned ZMK repository's `/.devcontainer/devcontainer.json` file. Add the volume under the "mounts" key: `"type=volume,source=zmk-localvolume,target=/workspaces/zmk-localvolume",`