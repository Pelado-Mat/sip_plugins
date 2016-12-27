SIP Pump Control Plugin
=======================

A plugin to interface with an arduino based Pump Control, see *pumpControl/pumpControl.ino* for the arduino code.
The Arduino is connected to the rPI via I2C to relay the pressure transducer pressure and get informed of the different alarms.
To control the pump relay, the arduino is conected between the master station pin (from the rPI)and the relay.

The arduino monitors that the pump is working correctly via a pressure transducer and controls the relay of the pump,
checking that the pressure is in a defined operational range.

It uses a Blinker alarm signal when detects some alarm on the pump.

Tested Platform
----------------
The arduino code is developed and tested with an _Arduino Nano_ and an _Aduino Uno_ (both clones). 
In production an _Arduino Nano_ is currently in use. The pressure transducer is an automotive oil-water sensor sourced in eBay.

Todo
--------------

* Add a i2C command to turn on the relay
* Add a sensor to know if the pump is really working ( there is a pump protector that cuts power if the current is too high)
* Think if It's desirable to sense the well water level in this plugin or in other one.
