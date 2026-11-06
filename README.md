# tinypico_sensor_board

This is a small motherboard for the TinyPICO to connect sensors to a QWIIC/STEMMA QT or Grove connector.

It supports three different configurations for the voltage on the connectors, to suppport the maximum number of sensors.

 - 3.3V power - 3.3V signal
 - 5V power, 3.3V signal
 - 5V power, 5V signal

See the PDF file for configuration options.

# Schema

See the PDF file for schematics.

# PCB

Designfiles in EAGLE format can be found in the `pcb` folder. Gerber files can be found in the `pcb/Gerber` folder.

# Firmwares

Firmware for connecting sensors to MQTT through this board is in the [Arduino_GroveSensors_Firmware](https://github.com/jonnybergdahl/Arduino_GroveSensors_Firmware) repository. It includes sketches for the Grove CO2 sensor, the Grove Multichannel Gas Sensor and the ZH03B particle sensor.

## Connectors

The QWIIC/Stemma QT port is connected to the default I2C pins of the TinyPICO, GPIO21 and GPIO22. 

The Grove connector is connected to GPIO5 (SDA) and GPIO4 (SCL), so to use I2C you need to initialize it with `Wire.begin(5, 4)`.

Note that the ESP32 allows you to assign any function to any pin, so any communication type is possible, like UART.
