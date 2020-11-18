# Flashing Microcontrollers


Each station node is build atop a microcontroller, where each
microcontroller is connected to one or more sensors either directly or
by [Grove hubs](https://www.seeedstudio.com/Grove-I2C-Hub.html). 

IotWx is designed to be used with the [m5Stack Atom Lite](https://m5stack.com/collections/m5-core/products/atom-lite-esp32-development-kit)
ESP32-Pico based microcontroller.  

There are two nodes that the core Arduino code has been developed for.
Before compiling the microcode onto the Arduino, you will also need to
install the core IoTwx shared library which controls many of the
communications and initialization functions of each node.

This core library can found at the following repository. It should be
installed in your `Arduiono/libraries` directory and once installed, you
may use it by the `#include "IoTwx.h"` directive.


* [https://github.com/NCAR/esp32-atomlite-arduino-iotwx](https://github.com/NCAR/esp32-atomlite-arduino-iotwx)

Please see the
[parts list](https://drive.google.com/file/d/1lAb784yfsxWOiH-yVCXQ3Ii0yEgUmtUQ/view?usp=sharing)
for the microcontroller, sensors and cables required or recommended to
build and connect a base system.


## Preparing Your System

You will need to install the [latest version of Arduino](https://www.arduino.cc/en/Main/Software) on your system to begin.

There are a few other steps you will need to complete:

* install the required ESP32 Pico / M5 Stack Atom lite boards; a comprehensive instruction set is [here](https://docs.m5stack.com/#/en/arduino/arduino_development)
* install the [arduino-esp32fs-plugin](https://github.com/me-no-dev/arduino-esp32fs-plugin) that will allow SPIFFS file uploads to ESP32 boards
* install the following libraries through the Arduino IDE:
   * MQTT library from 256dpi [https://github.com/256dpi/arduino-mqtt](https://github.com/256dpi/arduino-mqtt)
   * SeeedStudio VEML6070 library [https://github.com/Seeed-Studio/Seeed_VEML6070](https://github.com/Seeed-Studio/Seeed_VEML6070)
   * SeeedStudio BME280 library [https://github.com/Seeed-Studio/Grove_BME280](https://github.com/Seeed-Studio/Grove_BME280)
   * SeeedStudio BME680 library [https://github.com/Seeed-Studio/Seeed_BME680](https://github.com/Seeed-Studio/Seeed_BME680)
   * ArduinoJson library [https://github.com/bblanchon/ArduinoJson](https://github.com/bblanchon/ArduinoJson)
   * FastLED library [https://github.com/FastLED/FastLED](https://github.com/FastLED/FastLED)
   * NTPClient library [https://github.com/arduino-libraries/NTPClient](https://github.com/arduino-libraries/NTPClient)

## Atmos Node 

The Atmos node is comprised of two sensors and two 3d-printed housing
units. The first sensor houses the atmospheric conditions for air
temperature, humidity and barometric pressure. It can be fitted with the
[Seeedstudio BME280 Grove](https://www.seeedstudio.com/Grove-BME280-Environmental-Sensor-Temperature-Humidity-Barometer.html)
environmental sensor, or if you would like to obtain aggregate VOC
measurements, you can fit the housing with the
[BME680 Grove](https://www.seeedstudio.com/Grove-Temperature-Humidity-Pressure-and-Gas-Sensor-for-Arduino-BME680.html)
sensor. The code is designed to work with both sensors (but not
simultaneously). These parts can be found in the
[parts list](https://drive.google.com/file/d/1lAb784yfsxWOiH-yVCXQ3Ii0yEgUmtUQ/view?usp=sharing).


### Radiation Shield

<img width="360" alt="atmos node"
src="https://github.com/orgs/NCAR/teams/iotwx/master/img/atmos-node.jpg"/>

The radiation shield sensor captures the following measurements:
temperature, humidity, barometric pressure, and optionally VOC (if using
the BME680 sensor).

**PRINTING**

* the radiation shield design 3d print files can be found in the
  [`/build/stl/atmos`](https://github.com/NCAR/iotwx-manual/tree/master/build/stl/atmos) page. If you need to
  print, you will need to follow the instructions there to print the
  housing.

**FLASHING**

* the code to flash the node can be found in the
  [esp32-atomlite-arduino-atmos-node repository](https://github.com/NCAR/esp32-atomlite-arduino-atmos-node).
  You will to follow the instructions there to understand the Arduino
  flashing requirements and procedures.

### UV 

Because the UV measurement is part of the Atmos node, the code already
includes the capability to capture and transmit measurements. It is
integrated in to the
[esp32-atomlite-arduino-atmos-node repository](https://github.com/NCAR/esp32-atomlite-arduino-atmos-node)
and hence no other changes or files are necessary to flash once that
file has been uploaded to the microcontroller.


## Hydro Node

<img width="360" alt="hydro node"
src="https://github.com/NCAR/iotwx-manual/tree/master/img/hydro-node.jpg"/>
 
The hydro node is designed to collected and transmit precipitation
measurements.  

**PRINTING** 

* the rain gauge design 3d print files can be found in the
  [`/build/stl/hydro`](https://github.com/NCAR/iotwx-manual/tree/master/build/stl/hydro)
  page. If you need to print, you will need to follow the instructions
  there to print the housing.

**FLASHING**

* the code to flash the node can be found in the
  [esp32-atomlite-arduino-hydro-node repository](https://github.com/NCAR/esp32-atomlite-arduino-hydro-node).
  You will to follow the instructions there to understand the Arduino
  flashing requirements and procedures.

## Aero Node

<img width="360" alt="aero node"
src="https://github.com/NCAR/iotwx-manual/raw/master/img/wind-node.jpg"/>

The aero node is designed to collect wind vane & anemometer wind speed
and direction.

* Instructions for printing and flashing are forthcoming.
