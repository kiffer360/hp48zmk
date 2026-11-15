# HP48 ZMK config (nice!nano, 48 keys, PS/2 TrackPoint)

    .github/workflows/build.yml   GitHub Actions build
    boards/shields/hp48/          shield: 8x6 matrix, 4x12 key map, PS/2 nodes
    config/hp48.keymap            keymap (3 layers + auto mouse layer)
    config/hp48.conf              Kconfig options (USB logging on for testing)
    config/include/mouse_tp.dtsi  TrackPoint behaviors & settings
    config/west.yml               ZMK fork with mouse support + PS/2 driver module
    zephyr/module.yml, build.yaml

Before you push: change the URL in boards/shields/hp48/hp48.zmk.yml.

PS/2 and TrackPoint parts are adapted from infused-kim's example config:
https://github.com/infused-kim/kb_zmk_ps2_mouse_trackPoint_driver-zmk_config

Wiring: green (clock) -> D1, white (data) -> D0, red -> VCC (3.3V),
blue -> GND, 4.7k-10k pull-ups from clock and data to VCC.
