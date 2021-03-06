LSM9DS0 9-axis motion sensor with MPL3115A2 pressure sensor/altimeter mini add-on shield for the Teensy 3.1 microcontroller.

This sketch and library are specifically for the [LSM9DS0MiniTeensyShield.v05](https://www.oshpark.com/profiles/PeskyProducts/page/2)
which has been hardwired for I2C communication using the i2c_t3.h Wire library specifically designed for use with the Teensy 3.1.

There is only one way to install the Mini shield, at the end opposite the USB port either above or below the Teensy 3.1 proper.
Either way, SDA/SCL will be on pins 17 and 16, respectively, power and ground will be the two corresponding pins on the bottom
edge of the Teensy 3.1, and the other pin assignments are as follows: DRDYG is on pin 12, INTG on pin 11, DENG on pin 10, 
INT1 and INT2 for the pressure sensor are on pins 9 and 8, respectively. INT1XM and INT2XM are on pins 13 and 14, respectively,
and finally, the accel/gyro address pin ADO is on pin 15.

I recommend mounting the add-on shield below the Teensy 3.1 since the pressure sensor is somewhat light sensitive and mounting below
will provide some light screening. Also, mounting above will complicate access to the Teensy 3.1 reset button.

When properly mounted, the x-axis, which is the reference axis for True North is perpendicular to the Teensy 3.1 long axis.
The accel/gyro axis orientation is printed on the add-on shield.

The add-on shield has 10 kOhm pullup resistors on board with a jumper that can be adjusted to disable them if other
pullups are already in the circuit. However, this is impossible to do once the board is mounted so adjust your configuration 
accordingly. Perhaps in a future revision I will move the jumpers to the back of the Teensy 3.1 add-on shield for easier
re-configuration.

This add-on shield is one of many designed as part of the [Modular Teensy project](https://github.com/kriswiner/LSM9DS0/wiki/Modular-Teensy-Project).

For a  general discussion of motion sensing and sensor fusion, see [here](https://github.com/kriswiner/MPU-6050/wiki/Affordable-9-DoF-Sensor-Fusion).
