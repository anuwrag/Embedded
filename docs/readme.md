# Pinout for Heltec Wifi Kit 32 

# Setting up MicroPython on Heltec WiFi Kit 32 V3

This guide will walk you through setting up MicroPython on your Heltec WiFi Kit 32 V3.

## Prerequisites

* **Heltec WiFi Kit 32 V3:** Your ESP32 development board.
* **Computer:**  With Windows, macOS, or Linux.
* **USB Cable:** A micro-USB cable.
* **MicroPython Firmware:** Download the latest stable version from [micropython.org/download](micropython.org/download). I am using https://micropython.org/download/ESP32_GENERIC_S3/ latest firmware (v1.24.1 (2024-11-29).bin)
* **Mu IDE** I am testing on Mu IDE but feel free to choose your own.

## Installation Steps

### 1. Install ESPTool on your comptuer

Use pip to install the ESPTool:

```bash
pip install esptool # allows flashing of the esp firmware
pip install adafruit-ampy # allows transfer of data from computer to board

esptool.py --chip esp32 --port /dev/ttyUSB0 erase_flash
esptool.py --chip esp32 --port /dev/ttyUSB0 write_flash -z 0x1000 micropython-esp32-xxxx.bin

