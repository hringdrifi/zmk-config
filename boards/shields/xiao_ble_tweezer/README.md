# XIAO BLE Tweezer

Minimal three-key ZMK shield for testing BLE on a Seeed Studio XIAO nRF52840.

Short a pin to `GND` with tweezers:

```text
D0 -> A
D1 -> B
D2 -> C
```

For the Zephyr 3.5 based ZMK setup used by this repository:

```yaml
include:
  - board: seeeduino_xiao_ble
    shield: xiao_ble_tweezer
```

For current ZMK main/HWMv2:

```yaml
include:
  - board: xiao_ble//zmk
    shield: xiao_ble_tweezer
```

Double-tap reset on the XIAO nRF52840 to enter the UF2 bootloader, then copy
the generated UF2 to the mounted drive.
