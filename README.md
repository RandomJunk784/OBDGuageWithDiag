# OBDGuageWithDiag

ESP32-based read-only OBD-II visual diagnostic gauge.

## Current direction
- ESP32 handles TFT driving, UI, logic and Bluetooth-side communications.
- 2.1-inch TFT is the prototype display.
- External Bluetooth ELM327 provides the OBD-II data link.
- USB-C provides power/programming to the gauge electronics.
- Pico is intentionally removed from the proposed final architecture.
- Simple black-background digital UI.

## Safety boundary
The vehicle interface is **read-only**. Production firmware must not send ECU coding, adaptation, actuator, arbitrary CAN or other vehicle-control commands.

## Documentation
- [Architecture](docs/ARCHITECTURE.md)
- [Roadmap](docs/ROADMAP.md)
- [Safety boundary](docs/SAFETY.md)

This repository is the development home for the OBD diagnostic display project.
