Firmware support BTT Relay 1.2

Set pin PD14 and PF8 to high on startup:
Add "PD14,PF8" to "GPIO pins to set at micro-controller startup (NEW)"
If want to set low, input "!PD14,!PF8"