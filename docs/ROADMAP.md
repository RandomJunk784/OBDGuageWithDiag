# Development Roadmap

1. Prove ESP32 can drive the 2.1-inch TFT using the existing Pico display concept translated to C/C++.
2. Establish a stable screen/UI framework.
3. Connect ESP32 to the known-working Bluetooth ELM327 on the development van.
4. Implement read-only ELM327 initialisation and PID polling.
5. Display live values on the TFT.
6. Implement diagnostic readout using standard OBD-II DTC requests.
7. Add screen switching and a physical input/button.
8. Measure update rates, connection reliability and startup behaviour.
9. Test across additional known-compatible vehicles before defining supported-vehicle claims.
10. Package the electronics into the gauge housing.

Development rule: prove each layer independently before combining it.
