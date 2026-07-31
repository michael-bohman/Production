# ✅ Z9P GPS Board Programming

## Required Equipment/Materials

* RTK/PPK Module box&#x20;
* F9P GPS Board Programming Bag
* Computer

## Prep&#x20;

The following steps are only required for the first time doing this. The only exception is the firmware update that may be updated in the future.

1. Find and modify the 32014-02 Program
   1. Navigate to the following folder:
      1. \as-taurus.jdnet.deere.com\Production\Technical Packages\RTK PPK UNIT\IN PROGRESS\Programming\RTK-PPK Air Module
   2. Copy the 'Air Module' folder to anywhere on your machine.
   3. Right Click on 'program-32014-02' and click 'Edit in Notepad'.
   4. On the 3rd line, you should find
      1. SET ipeCmd="C:\Program Files (x86)\Microchip\MPLABX\v5.20\mplab\_platform\mplab\_ipe\ipecmd.exe"
   5. On the 4th line, you should find
      1. SET pgmDev=PK3
   6.

       <figure><img src="../../.gitbook/assets/image (239).png" alt="" width="563"><figcaption></figcaption></figure>
   7. Save and close notepad.
2. Download the Firmware Update if needed
   1. Navigate to the link [https://www.u-blox.com/en/products/zed-f9p-module?legacy+Current#Documentation-&-resources](https://www.u-blox.com/en/products/zed-f9p-module?legacy+Current#Documentation-&-resources)
   2. Scroll down and click 'Documentation & Resources'
   3. Click 'Firmware Update'.
   4. Download the Latest version and place this file in your 'ROVER6\_A' folder.&#x20;

## Guide

### GPS Programming&#x20;

1. In the RTK/PPK Modules Box
   1. Plug in the GPS Board to your computer using both the PICkit™3 and a usb cable

<figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

2. Program the board.
   1. Open ‘program-32014-02.bat’.
   2. After the board is programmed, it will say ‘Board program successful, press any key to exit’.

<figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>

3. Check that the LEDs are illuminated as required
   1. Status LED: Flashing
      1. If it is not illuminated, disconnect everything and place the board in a bag and mark 'BAD'. Contact Alex Stephens to see if it can be fixed
   2. Heartbeat LED: Flashing
      1. If the heartbeat is not flashing or illuminated, ensure the status LED is working, then continue with the build. The Heartbeat LED is not seen by the customer and does not affect the integrity of the board, just means that light does not work.&#x20;

<div><figure><img src="../../.gitbook/assets/image (242).png" alt="" width="231"><figcaption><p>Status LED</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (243).png" alt="" width="230"><figcaption><p>Heartbeat LED</p></figcaption></figure></div>

4. Exit the program and unplug everything.

### GPS Firmware Update

1. Open U-Center
2. Plug in the GNSS board to your computer using only a USB-C cable.
3. At the top, click on the upside-down triangle next to the connection symbol and select the corresponding COM Port

<figure><img src="../../.gitbook/assets/image (244).png" alt="" width="563"><figcaption></figcaption></figure>

4. At the top, click Tools>Firmware Update...
   1.

       <figure><img src="../../.gitbook/assets/RTK-PPK firmware update image .png" alt=""><figcaption></figcaption></figure>



#### Firmware Update Utility Window&#x20;

1. In the new window, click on the 3 dots next to the 'Firmware image' box.
2. Find the File&#x20;
3. and click 'Open'.
4. To speed up the update process, a higher baud rate may be used, just ensure that it updated correctly afterwards.
   1. 9600 baud results&#x20;
   2. Use 921600 if the first baud rate is slow&#x20;
5. Click 'GO' at the bottom

<figure><img src="../../.gitbook/assets/image (245).png" alt="" width="563"><figcaption></figcaption></figure>

9. Once the update has completed, at the top, go to View>Messages View>UBX>MON>VER
   1. Verify the Version number is 1.51

{% hint style="info" %}
The tree viewer is slightly too skinny. Use the scroll bar at the bottom to slide left and minimize the NMEA branch.
{% endhint %}

10. Power Cycle the board and ensure the status LED doesn't flash.

{% hint style="warning" %}
If you are doing multiple boards, keep Ucenter open in the background. You will have connectivity issues if you keep closing the application.&#x20;
{% endhint %}
