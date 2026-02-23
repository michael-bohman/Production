# Board Programming

## Required Materials

* TTL Cable with 4 pin adapter
* 12V AC Power Adapter
* Anderson to power adapter
* green ribbon cable
* Leveling board
* Level

## Notes

The process of programming these board is very similar to that of the 6x/65R. The main differences are the cables.

## Guide

{% stepper %}
{% step %}
### Level the Surface

Note: The level on the leveling board is inaccurate. Place a level on top of the board for an accurate reading.

1. Screw in all the feet of the leveling board.
2. Place the level on the board in a front-to-back orientation.
3. While the level is on the board, unscrew the two feet on the low side (away from the bubble) until the bubble is centered.
4. Repeat this with the level perpendicular to step 2.
5. Double check that the board shows level when the level is in any orientation.
6. Ensure the board does not wobble at all.
   1. If the board wobbles at all, unscrew one of the two feet that it is wobbling between and double check levels, repeat if needed.
{% endstep %}

{% step %}
### Plug In Everything

Plug in all the cables as follows: (Note: Wait to plug in the Anderson power pole connection)

* Computer to board via TTL cable and adapter.
  * Plug into CTRL UART port on board.
* Power Adapter into EXT PWR I/O port on board.
* AC Adapter into wall outlet.

<figure><img src="../../../.gitbook/assets/IMG_7684.jpg" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Follow Steps in Partner Assistant (MISSING SERIAL NUMBER STEP)

1. Switch the 'CTRL PROG' Switch on the board to 'ON'.
2. Plug in the Anderson Power Pole connection.
3. Open Basecam Simple BGC Partner Assistant.
   1. If the serial number required is not known, click on 'Web Control Panel'. Sign in and click 'Customers' and the top. The required serial number will be the next highest.
4. Click on the drop down in the top left corner and ensure the correct COM port is selected.
   1. Do NOT click 'Connect'
5. Click 'Test Board'
6. Select license #5033 and click 'upload'.
7. After it is completed, select firmware 2.70.0 ENCODERS and click 'upload'.
8. Once it finishes and gets to the page with the check marks and red x, click cancel and unplug the power connection to the board.
9. flip the 'CTRL PROG' switch to 'OFF'.
{% endstep %}

{% step %}
### Upload the Backup

1. connect the green ribbon cable between the two boards.
2. place the other board into the jig, screw down lightly to preserve the threads bubt tight enough that it won't move.
3. Open Basecam GUI.
4. Reconnect the power cable to the board.
5. Towards the top, ensure the correct COM port is selected. Click 'Connect'.
6. At the top, click 'Board'>'Backup Manager'.
7. In the lower 'backup' section, click browse.
8. Find the correct Pixelscout Phase 4 EEPROM file and select 'Upload'.
{% endstep %}

{% step %}
### Calibrate the IMU

1. Navigate to the 'Hardware' tab on Basecam GUI.
2. Click on 'Calibrate IMUs'.
3. In the IMU Calibration side (Left), click 'Reset'.
4. orient the board in the jig on any face, wait for the bar on the right to reach green, click 'Calibrate' and repeat for another face until all 6 are checked.
5. Once the board IMU is calibrated, export the calibration data to the corresponding SN folder in taurus.
6. At the top, click 'Disconnect' and disconnect all of the board connections.
{% endstep %}
{% endstepper %}
