# Hringbord Segl ZMK board

This is a ZMK keyboard-board port of the QMK `keyboards/hringbord/segl`
definition. Segl has an RP2040 mounted on the PCB, so this is modeled as a
board rather than a shield.

The QMK definition uses the same 11 GPIOs for rows and columns with the
diagonal masked out. In ZMK this maps naturally to `zmk,kscan-gpio-charlieplex`;
the matrix transform preserves the QMK `LAYOUT` order from `keyboard.json`.

GPIO order:

```text
GP20, GP19, GP18, GP17, GP16, GP3, GP9, GP10, GP11, GP8, GP25
```

Build target:

```sh
west build -p -b segl//zmk
```
