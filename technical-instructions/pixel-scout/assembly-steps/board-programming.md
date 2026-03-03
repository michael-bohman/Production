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

### Preparation

1. Level the leveling board using an external level.
2. Open Partner Assistant and log in.
3. Connect one end of the green microcoax cable to the 'Gimbal' port on the end of the pixelscout breakout board.
4. Place the Pixelscout breakout board into the rectangular jig and secure barely snugly using the 2 black course threaded screws included.
5. Plug in all the required connections **except the anderson power pole connection.**
   1. Computer to board via TTL cable and adapter.
      * Plug into CTRL UART port on board.
   2. Power Adapter into EXT PWR I/O port on board.
   3. AC Adapter into wall outlet.

<figure><img src="../../../.gitbook/assets/IMG_7684.jpg" alt="" width="375"><figcaption></figcaption></figure>

6. Switch the 'CTRL PROG' Switch on the SBG Breakout Board to 'ON'.

### Programming Steps

#### Partner Assistant

{% hint style="info" %}
If the serial number required is not known, click on 'Web Control Panel'. Sign in and click 'Customers' and the top. The required serial number will be the next highest 23138-03\_rev- Serial Number.
{% endhint %}

1. Click on the drop down in the top left corner and ensure the correct COM port is selected.

{% hint style="warning" %}
Do NOT click 'Connect'
{% endhint %}

2. Click 'Test Board'
3. Select '3.3 "Tiny+"'. and click 'FLASH'.
4. Select/Adjust the following settings and click 'Next'.
   1. License: **#5033**
   2. 3 axis driver: **unchecked**
   3. Battery Voltage Sensor: **Checked**
   4. Motor Power: **80**

{% hint style="info" %}
NOTE: some errors may pop up. This is okay, just click 'OK'.
{% endhint %}

5. In the 'Flash new secret keys' page, click 'Next'.
6. Select/Adjust the following settings and click 'Next'.
   1. 3 axis driver: **unchecked**
   2. Battery Voltage Sensor: **Checked**
   3. Reference Voltage: **12.05 V**
   4. Reference Current: **0 A**
   5. Board ID: **23138-03\_rev-\_SNXXX.** (where XXX denotes the next few numbers from the Basecam website.
7. After it is completed, select firmware 2.70.0 ENCODERS and click 'upload'.
8. Once it finishes and gets to the page with the check marks and red x, click cancel and unplug the power connection to the board.
9. flip the 'CTRL PROG' switch on the SBG Breakout Board to 'OFF'.

#### Basecam SimpleBGC GUI

1. Connect the other end of the green microcoax cable to the 'Gimbal' connection on the Pixelscout Breakout Board.
2. Open 'SimpleBGC GUI'.
3. Reconnect the power cable to the board.
4. Towards the top, ensure the correct COM port is selected. Click 'Connect'.

{% hint style="info" %}
Notes:&#x20;

1. Some errors may pop up. That is okay. just click 'OK'.&#x20;
2. The main error that might come up is 'Serial Data Corrupted'. If this happens, check that the 'CTRL PROG' switch on the SBG Breakout Board is set to 'OFF' and power cycle the board.
{% endhint %}

1. At the top, click 'Board'>'Backup Manager'.
2. In the 'Restore from backup' section, click browse.
3. Find the Pixelscout Phase 4 'Starting Point' EEPROM file and select 'Open', then 'Restore'.
4. Navigate to the 'Hardware' tab on Basecam GUI.
5. Click on 'Calibrate IMUs'.
6. In the 'Accelerometer' side (Left), click 'Reset'.
7. Orient the board in the jig on any face, wait for the bar on the right to reach green, click 'Calibrate' and repeat for another face until all 6 are checked.
8. Once the board IMU is calibrated, export the calibration data.
   1. At the bottom of the 'Sensor Calibration Helper' window, click 'Backup...'.
   2. Name: sbgc\_IMU\_calib\_phase4SNXXX' where 'XXX' denotes the pixel scout gimbal serial number.
   3. Folder: New folder titled the 3 digit serial number
   4. Click 'Save' and then 'Close'.
9. Board Programing is complete! At the top, click 'Disconnect' and disconnect all of the board connections.
