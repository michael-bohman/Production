# Board Programming

## Required Materials

* TTL Cable with 4 pin adapter
* 12V AC Power Adapter
* Anderson to power adapter
* green ribbon cable

## Notes

The process of programming these board is very similar to that of the 6x/65R. The main differences are the cables.

## Guide

Stepper blocks let you break down a tutorial or guide into separate, but clearly linked steps. Each step can contain multiple different blocks, allowing you to add detailed information.

{% stepper %}
{% step %}
### Plug In Everything

Plug in all the cables as follows: (Note: Wait to plug in the Anderson powerpole connection)

* Computer to board via TTL cable and adapter.
  * Plug into CTRL UART port on board.
* Power Adapter into EXT PWR I/O port on board.
* AC Adapter into wall outlet.

<figure><img src="../../../.gitbook/assets/IMG_7684.jpg" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Follow Steps in Partner Assistant (MISSING SERIAL NUMBER STEP)

1. Switch the 'CTRL PROG' Switch on the boadr to 'ON'.
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


{% endstep %}
{% endstepper %}
