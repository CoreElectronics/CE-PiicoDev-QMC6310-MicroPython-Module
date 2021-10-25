<!-- TODO How to use this template
Follow these commented instructions to build the repo.
Delete the instructions as you go, to keep for a cleaner final file.
 -->

<!-- TODO Initialise the repo with the following two files:
 The MicroPython Module for this device with name: "PiicoDev_[DEVICE MFN].py". Eg for temperature sensor TMP117: PiicoDev_TMP117.py
 A (tested) main.py file
-->


<!-- TODO update title to be descriptive. Eg.
PiicoDev® [Description] [Part#] MicroPython Module
PiicoDev® Precision Temperature Sensor TMP117 MicroPython Module -->
# PiicoDev® Template MicroPython Module

<!-- TODO update link URL with CE SKU -->
<!-- TODO update link title -->
This is the firmware repo for the [Core Electronics PiicoDev® XXXXXX](https://core-electronics.com.au/catalog/product/view/sku/XXXXXX)

This module depends on the [PiicoDev Unified Library](https://github.com/CoreElectronics/CE-PiicoDev-Unified), include `PiicoDev_Unified.py` in the project directory on your MicroPython device.

<!-- TODO update tutorial link with the device tinyurl eg. piico.dev/p1
See the [Quickstart Guide](https://piico.dev/pX)
 -->

<!-- TODO verify the tested-devices list -->
This module has been tested on:
 - Micro:bit v2
 - Raspberry Pi Pico
 - Raspberry Pi SBC

## Details
### `PiicoDev_QMC6310(bus=, freq=, sda=, scl=, addr=0x1C)`
Parameter | Type | Range | Default | Description
--- | --- | --- | --- | ---
bus | int | 0,1 | Raspberry Pi Pico: 0, Raspberry Pi: 1 | I2C Bus.  Ignored on Micro:bit
freq | int | 100-1000000 | Device dependent | I2C Bus frequency (Hz).  Ignored on Raspberry Pi
sda | Pin | Device Dependent | Device Dependent | I2C SDA Pin. Implemented on Raspberry Pi Pico only
scl | Pin | Device Dependent | Device Dependent | I2C SCL Pin. Implemented on Raspberry Pi Pico only
addr | int | 0x1C | 0x1C | This address cannot be changed

### `PiicoDev_QMC6310.readTruePolar(declination=)`
Reads the calibrated magnetic field magnitude and angle in the X and Y plane.

### `PiicoDev_QMC6310.readPolarCal()`
Reads the calibrated magnetic field magnitude and angle in the X and Y plane.

### `PiicoDev_QMC6310.readPolar()`
Reads the raw magnetic field magnitude and angle in the X and Y plane.

### `PiicoDev_QMC6310.read()`
Reads the X, Y and Z components of the magnetic field.

### `PiicoDev_QMC6310.calibrate()`
Routine to calibrate the magnetometer.

# License
This project is open source - please review the LICENSE.md file for further licensing information.

If you have any technical questions, or concerns about licensing, please contact technical support on the [Core Electronics forums](https://forum.core-electronics.com.au/).

*\"PiicoDev\" and the PiicoDev logo are trademarks of Core Electronics Pty Ltd.*
