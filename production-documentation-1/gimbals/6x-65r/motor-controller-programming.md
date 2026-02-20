# Motor Controller Programming

## Items Required

* 12V AC Power Adapter
* TTL USB Cable
* Y-connector
* Power I/O cable

## Programming Guide

1. Carefully pull up the Kapton Tape from the board and flip the switch to the 'ON' position.
2. Plug in all the required connections:
   1. AC Adapter (12V) into outlet.
   2. TTL USB cable into computer.
   3. Motor controller board to USB cable via Y adapter cable.
   4. Motor controller board to AC Adapter via Y adapter cable.
      1. Connect Anderson Power Pole connector LAST.
3. Open Partner Assistant.
4. At the top, click on the upside-down triangle and select the COM port associated with the TTL cable.

{% hint style="warning" %}
NOTE: Do NOT click 'Connect'.
{% endhint %}

5. If the intended serial number is not know, click on 'Web Control Panel'.
   1. Log in and go to 'Customers'.
   2. Note the last used serial number for the corresponding part number. Use the following number(s).
6. Click 'Test Board'.
7. Select the following board version and click 'Flash'.

```
3.3 "Tiny+" (256K) - low power, small size board
```

{% hint style="info" %}
If any errors occur, that is OK. Just click next.
{% endhint %}

8. Select the following license and click 'NEXT >'.

```
#2033
```

9. Once the 'Board ID' box displays, change the last few numbers to match the intended serial number form step 5. Click 'NEXT >'.
10. Select the following firmware number and click 'UPLOAD'.

```
2.70.0
```

11. Once you have reached the screen that says 'Finished!' and 'Congratulations! You have finished configuring the board!'. Click 'Cancel'.
12. Disconnect all the connections to the board.

{% hint style="info" %}
If camera pairing/IMU Calibration will be performed immediately, everything may stay connected except the power. Disconnect using the Anderson connector for a cleaner disconnect.
{% endhint %}

13. Carefully flip the switch on the board to 'OFF'.





## IMU Calibration Guide

{% hint style="warning" %}
NOTE: This step should be completed using the camera intended to be used with the motor controller. Using a different camera may result in imperfect IMU calibration when on the gimbal.
{% endhint %}

{% hint style="info" %}
This instruction set is the same for 6X and 65R cameras, pictures show the 65R.
{% endhint %}

1. Set up the leveling board.
   1. Screw in all feet completely and unscrew 2 adjacent feet at the same time as needed to level the board

{% hint style="warning" %}
The built-in level in the board is not accurate, an external level should be used for an accurate orientation.
{% endhint %}

2. Plug in all the required connections:
   1. AC Adapter (12V) into outlet.
   2. TTL USB cable into computer.
   3. Motor controller board to USB cable via Y adapter cable.
   4. Motor controller board to AC Adapter via Y adapter cable.
      1. Connect Anderson Power Pole connector LAST.
   5. Motor controller to camera via cable.
3. Open the 'Simple BGC GUI v2.7.0' program.
4. Select teh COM port assosiated with the TTL cable and click 'Connect'.
5. Some errors might be present. This is OK. Just click 'OK'.
6. At teh top, go to 'Board'>'Backup Manager'.
7. In the 'Restore from Backukp' section, click 'Browse'.
8. Find and upload the correct EEPROM file.
   1. 65R EEPROM: '65RMotorController.data'.
   2. 6X EEPROM: 'asdf'.
   3. Navigate through the 'Essentials' folder on the desktop of brandon's laptop.

