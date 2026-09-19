# OBDGuageWithDiag — Architecture

## Purpose
Browser-independent, vehicle read-only diagnostic/display gauge built around an ESP32 and an external Bluetooth ELM327 interface.

## Hardware direction
- ESP32: display driver, UI, application logic.
- 2.1-inch TFT: primary display during prototype.
- Bluetooth ELM327: OBD-II data transport.
- USB-C: power/programming connection to the ESP32.
- No Pico in the final architecture unless testing proves it necessary.

## Vehicle safety boundary
The gauge is read-only with respect to the vehicle ECU/OBD interface.

It must not:
- write ECU data
- code/program modules
- perform adaptations
- actuate outputs
- send arbitrary CAN commands
- clear diagnostic trouble codes in the first production design

The ELM327 link is treated as a data source only.

## Intended UI
Simple black-background digital displays. Priorities are clarity, low latency and useful diagnostics rather than graphical complexity.

Possible screens include:
- boost/MAP
- RPM
- coolant temperature
- intake/air temperature
- calculated load
- vehicle speed
- throttle position
- fuel-related values where supported
- diagnostic trouble-code list
- connection/status screen

Not every PID is available on every vehicle.
