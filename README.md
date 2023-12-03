# HWF03TEM

HW Description of the HWF03TEM-01-V1.0 Smart Din Rail Switch

Also sold as OP-DRWF01 and under the Smartgrade brand

## ESPHome configuration

Included in this repository is a ESPHome yaml for the device.

### What works
* pushbutton - manually open/close the relay
* Control for the additional LED
* calibrated *Current/Voltage monitor

### What doesn't
* Couldn't get Power monitor to work, but its basically I * V

## Product images
![productimage1](https://github.com/yonirom/HWF03TEM/blob/main/assets/1.jpg?raw=true)
![productimage2](https://github.com/yonirom/HWF03TEM/blob/main/assets/2.jpg?raw=true)

# Hardware
HWF03TEM-02-v1.0

MCU: Tuya TYWE3S [info](https://tasmota.github.io/docs/devices/TYWE3S/)


## MCU Daughterboard
Connections between the 6 pin JST to the MCU GPIO pins
```text
* * * * * *
| | | | | |
| | 12| | |
| en  4 | gnd
vcc     5
```

* GPIO0 -> User facing pushbutton
* GPIO14 -> Relay and two blue leds active high
* GPIO13 -> Single blue led active low

## HLW8012 - Voltage/Current/Power monitor IC
TYWE3S  |HLW8012
--------|-------
GPIO12  |Sel
GPIO4   |CF
GPIO5   |CF1

Additional [info](https://esphome.io/components/sensor/hlw8012)
