# Safety Boundary

This project is deliberately designed as a read-only vehicle information display.

## Hard rule
No production firmware may transmit vehicle-control, coding, adaptation or actuator commands.

Diagnostic functionality should initially be limited to reading standard diagnostic information and presenting it to the user.

If a future feature would require transmitting anything beyond the minimum read request required by the chosen diagnostic protocol, stop and review it before implementation.

During bench work: disconnect vehicle power before soldering or modifying wiring. Do not solder on a powered circuit.
