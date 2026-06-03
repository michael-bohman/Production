---
description: 'Owner: Amanda Janssen'
---

# 📷 Gimbal Stack

## Equipment

<table><thead><tr><th>COMS Boards</th><th valign="middle">Motor Controllers</th></tr></thead><tbody><tr><td>Non-John Deere Laptop</td><td valign="middle">TTL USB Cable</td></tr><tr><td>MPLAB ICE module (with USB cable and small cable)</td><td valign="middle">Y-connector</td></tr><tr><td>24V "NEW COMMS BOARD ONLY" AC Adapter</td><td valign="middle">12V AC Power Adapter</td></tr><tr><td>Anderson power adapter cable</td><td valign="middle">Power I/O cable</td></tr><tr><td>communication adapter cable</td><td valign="middle">Tweezers </td></tr></tbody></table>

## Notes

* Cables and Power Adapters will be located in labeled bags located next to laptop
* This guide is for 6X and 65R gimbals&#x20;

## Coms Board Programming Guide

1. Plug in everything
   1. PLUG IN ANDERSON CONNECTOR LAST to avoid any unwanted power surges or dips.
   2. Power via ac adapter and Anderson power adapter cable
   3. Communication from computer via MPLAB ICE comms box and adapter
   4.

       <figure><img src="../../../.gitbook/assets/image (170).png" alt="" width="563"><figcaption></figcaption></figure>


2. Open the MPLAB X IPE v5.2 Software&#x20;
   1. Application should be located on the desktop&#x20;
3. Program the board
   1. Under 'Device:',confirm the model number of the PIC32 chip on the comms board
      1. The model number is on one side of the black microchip on the board.
      2. For 6X and 65R the model on the COMS board should be 'PIC32MX795F512L'.
   2.

       <figure><img src="../../../.gitbook/assets/image (171).png" alt="" width="563"><figcaption></figcaption></figure>


4. <mark style="color:blue;">Click connect</mark>
   1. The pink box at the bottom should populate
   2. 'Connect' button should now say 'Disconnect'
5. To the right of the 'Hex File' box, click on <mark style="color:blue;">Browse</mark>.
6. Find the correct hex file and open it into the program.
   1. Should be the first file you see (pic32-Gimbal2.DEFAULT3.2025073000.hex.)
      1. _Location of file if needed: \as-taurus.jdnet.deere.com\Production\Technical Packages\6X AND 65R GIMBAL\IN PROGRESS\6X AND 65R GIMBAL - Technical Data Package - ######\PROGRAMMING\Prerequisites and Programs\Hex File_
   2. Click <mark style="color:blue;">Open</mark> to load that file&#x20;
7. Once hex file is loaded click <mark style="color:blue;">Program</mark>&#x20;
8. The programming process will say completed and the COMs board should have a flashing green light alongside a solid red light.&#x20;

{% hint style="danger" icon="hand" %}
If the green light is not visible then click <mark style="color:blue;">program</mark> again. You should see the programming completed message and the flashing green light when finished.&#x20;
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (172).png" alt="" width="563"><figcaption></figcaption></figure>

9. Click <mark style="color:blue;">Disconnect</mark> and unplug the board, power first.
10. Put COMS board back in the Static Bag and mark it completed with Sharpie&#x20;

## Motor Controller Programming Guide

1. Carefully pull up all the Kapton Tape from the board and flip the switch to the 'ON' position.
2. Plug in all the required connections:
   1. AC Adapter (12V) into outlet
   2. TTL USB cable into computer
   3. Motor controller board to USB cable via Y adapter cable.
   4. Motor controller board to AC Adapter via Y adapter cable.
      1. Connect Anderson Power Pole connector LAST.

<mark style="color:$danger;">(Insert image for connections)</mark>

3. <mark style="color:blue;">Open Partner Assistant</mark> and login to your account
   1. Log into the Webpage now, or wait until future steps for instructions
4. At the top left corner, if the box is empty, click on the <mark style="color:blue;">upside-down triangle</mark> and select the <mark style="color:blue;">COM port</mark> associated with the TTL cable.

{% hint style="danger" %}
NOTE: Do NOT click 'Connect'.
{% endhint %}

5. Click <mark style="color:blue;">Test Board</mark>
6. Select the following board version below (Insert Page name)

```
3.3 "Tiny+" (256K) - low power, small size board
```

8. Click <mark style="color:blue;">Flash</mark>&#x20;
   1. <mark style="color:$danger;">(Insert Pic of screen when finished)</mark>
9. Select the following license below (Insert page name)

```
#2033
```

{% hint style="info" %}
If any errors occur, that is OK.
{% endhint %}

<mark style="color:$danger;">(Insert Pic of screen when finished)</mark>

9. Insert Serial number&#x20;
   1. In the Board ID box, change the last few numbers to the serial number following the last used on the web control panel page. See instructions below if not already logged into control Panel.

<details>

<summary>Web Control Panel (Insert Example)</summary>

If the intended serial number is not know, click on <mark style="color:blue;">Web Control Panel</mark>

1. Log in and go to <mark style="color:blue;">Customers</mark>
2. This website is only to view the last used serial number for the corresponding part number. In partner assist, use the next number in the series.&#x20;

</details>

<mark style="color:$danger;">(Insert Pic of screen when finished)</mark>

9. Select the following firmware number and click 'UPLOAD'.

```
2.70.0
```

11. Once you have reached the screen that says 'Finished!' and 'Congratulations! You have finished configuring the board!'. Click <mark style="color:blue;">Cancel</mark>
12. Disconnect all the connections to the board, power first.&#x20;
13. Carefully flip the switch on the board to OFF

### IMU Calibration Guide

{% hint style="warning" %}
NOTE: This step should be completed using the camera intended to be used with the motor controller. Using a different camera may result in imperfect IMU calibration when on the gimbal.
{% endhint %}

{% hint style="info" %}
This instruction set is the same for 6X and 65R cameras, pictures show the 65R.
{% endhint %}

1. Set up the leveling board.
   1. Screw in all feet completely and unscrew 2 adjacent feet at the same time as needed to level the board
2. Install the Calibration Jig on the camera using at least 2 screws, ensuring it will not move inside of it.

{% hint style="warning" %}
The built-in level in the board is not accurate, an external level should be used for an accurate orientation.
{% endhint %}

3. Plug in all the required connections:
   1. AC Adapter (12V) into outlet.
   2. TTL USB cable into computer.
   3. Motor controller board to USB cable via Y adapter cable.
   4. Motor controller board to AC Adapter via Y adapter cable.
      1. Connect Anderson Power Pole connector LAST.
   5.  Motor controller to camera via cable.

       <figure><img src="../../../.gitbook/assets/image (35).png" alt="" width="407"><figcaption></figcaption></figure>
4. Open the 'Simple BGC GUI v2.7.0' program.
5. Select the COM port associated with the TTL cable and click 'Connect'.
6. Some errors might be present. This is OK. Just click 'OK'.
7. At the top, go to 'Board'>'Backup Manager'.
8. In the 'Restore from Backup' section, click 'Browse'.
9. Find and upload the correct EEPROM file.
   1. 65R EEPROM: '65RMotorController.data'.
   2. 6X EEPROM: 'asdf'.
   3. Navigate through the 'Essentials' folder on the desktop of Brandon's laptop.
10. Click 'Restore'.
11. After this finishes, close the backup window and go to the 'Hardware' tab.&#x20;
12. Click 'Calibrate IMU Sensors...'.

{% hint style="warning" %}
Only use the left side of the IMU Calibration window. DO NOT click anything on the right side. Only use the right side for using the bar visual.
{% endhint %}

13. In the new window, on the left side, click 'Reset'.
14. Calibrate the accelerometer.
    1. Use the calibration jig and rest the camera on each side.
    2. After the gyroscope gauge rests in the green portion, click on the 'CALIBRATE' button in the 'Acceleromter' section.
    3. Repeat for all 6 sides.
15. After calibration is complete, click 'Close'.
16. Click 'Disconnect' and disconnect all the connections.

{% hint style="warning" %}
Try to keep the paried motor controller and camera together. Failing to do so may result in inaccurate calibrations.
{% endhint %}
