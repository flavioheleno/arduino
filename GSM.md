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

## AT Commands

Below is a list of useful AT Commands.

Command         | Description
----------------|------------
ATE1            | Enables command echo.
AT+CBAND?       | Queries the current band configuration.
AT+CBAND=?      | List all available band options.
AT+CBAND="X"    | Sets the band configuration.
AT+COPS?        | Queries the current operator.
AT+COPS=?       | List all available operators.
AT+COPS=0       | Sets the current operator to automatic.
AT+COPS=1,0,"X" | Sets the current operator manually.
AT+CSQ          | Queries the current signal strength (0-31).
AT+CREG?        | Queries the current registration status.
AT+CENG=1       | Enables engineering mode.
