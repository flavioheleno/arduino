# GSM

I have a SIM900 GSM Shield and I am using [TinyGSM](https://github.com/vshymanskyy/TinyGSM).

All I had to do to make it work was to change the GPRS jumper from SWSerial to Xduino (hardware).

Note that the jumper already connects GPRS-Rx to Arduino-Tx and GPRS-Tx with Arduino-Rx.

Code sample available at [examples/GSM.ino](examples/GSM.ino).

## Connections

Shield | Arduino
-------|--------
VCC    | 5V
GND    | GND
D0     | Pin 14 (TX3)
D1     | Pin 15 (RX3)
