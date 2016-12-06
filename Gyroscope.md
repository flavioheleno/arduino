# Gyroscope

I have a GY-521 (MPU-6050) shield that has both an accelerometer and a gyro in a single chip.

According to a few different links[[1](http://dummyscodes.blogspot.com.br/2014/07/mpu6050-gy-521-breakout-arduino-mega.html)][[2](http://forum.arduino.cc/index.php?topic=166113.0)] this shield has an onboard voltage regulator for 3.3V, which means that you can connect it to Arduino's 5V output without problems.

I'm using [I2CDevLib](https://github.com/jrowberg/i2cdevlib) to work with this shield, more specifically [this](https://github.com/jrowberg/i2cdevlib/tree/master/Arduino/I2Cdev) and [this](https://github.com/jrowberg/i2cdevlib/tree/master/Arduino/MPU6050).

## Connections

Shield | Arduino
-------|--------
VCC    | 5V
GND    | GND
SCL    | Pin 21 (SCL)
SDA    | Pin 20 (SDA)
INT    | Pin 2 (interrupt 0)

## Testing

You can user [I2C Scanner](http://playground.arduino.cc/Main/I2cScanner) to check if the shield communication with your arduino is working properly.

The scanner will scan all I2C devices and report to the Serial Monitor.

```
I2C Scanner
Scanning...
I2C device found at address 0x68  !
done
```

## Interrups

According to Arduino's [reference](http://arduino.cc/en/Reference/AttachInterrupt), Mega 2560 has 6 pins that can be used for interrupts: 2, 3, 18, 19, 20 and 21.
