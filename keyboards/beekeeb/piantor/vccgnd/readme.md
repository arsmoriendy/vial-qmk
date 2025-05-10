# VCC-GND RP2040 (YD-RP2040)

> [!note]
> Originally copied from `../estardyn/`, since there should be no hardware differences between the two..

Because of a difference in how `VIN` and `VOUT` (called `VBUS` and `VSYS` on the genuine Pico) are wired,
`USB_VBUS_PIN` cannot be used.

For the same reason as above, you will have to bridge the `VIN` and `VOUT` pins for the right half to be powered properly

The YD-RP2040 has a ws2812 wired to pin `GP23`. Both (one per half) have been enabled in this config and configured as layer indicator rgbs.
In addition it also has an LED wired to pin `GP25` as a caps lock indicator.

In order to enable the ws2812 RGB, you must bridge the the pads labeled `R68`/`RGB` located above the RGB module.
