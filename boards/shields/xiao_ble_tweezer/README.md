# XIAO BLE Tweezer

Minimal three-key ZMK shield for testing BLE on a Seeed Studio XIAO nRF52840.

Short a pin to `GND` with tweezers:

```text
D0 -> A
D1 -> B
D2 -> C
```

The shield includes metadata, so `zmk keyboard add` can discover it when this
folder is available in your `zmk-config` or an added ZMK module. Select:

```text
Keyboard/shield: XIAO BLE Tweezer
Controller: Seeed Studio XIAO nRF52840
```

The metadata uses the `seeed_xiao` interconnect ID. If controller candidates do
not appear, refresh the ZMK CLI metadata/cache or update the ZMK checkout used
by the CLI so it includes Seeed XIAO controller metadata.

Manual `build.yaml` entry for the Zephyr 3.5 based ZMK setup used by this
repository:

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
