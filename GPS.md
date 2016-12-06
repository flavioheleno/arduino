# GPS

I have a ublox-6m-0-001 GPS Shield and I'm using [TinyGPSPlus](https://github.com/mikalhart/TinyGPSPlus).

All code samples shipped with TinyGPSPlus use `SoftwareSerial` hooked to pins 4 (RX) and 3 (TX) with a 4800 Baud Rate.

That doesn't quite work right away, so I've replaced the `SoftwareSerial` with `Serial3` and hooked the shield to pins 15(RX) and 14 (TX) with 9600 Baud Rate.

Code sample available at [examples/GPS.ino](examples/GPS.ino).

## Connections

Shield | Arduino
-------|--------
VCC    | 3.3V
GND    | GND
TX     | Pin 15 (RX3)
RX     | Pin 14 (TX3)
