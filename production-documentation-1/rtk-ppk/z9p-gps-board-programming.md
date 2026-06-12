# 📷 Z9P GPS Board Programming

## Required Equipment/Materials

* F9P GPS Board Programming Bag
*

## Notes



## Prep&#x20;

The following steps are only required for the first time doing this. The only exception is the firmware update that may be updated in the future.

1. Find and modify the 32014-02 Program
   1. Navigate to the following folder:
      1. taurus\Data\Part Database (things we sell)\SW-32014 -- ZED F9P\\
   2. Copy the 'ROVER6\_A' folder to anywhere on your machine.
   3. Open file explorer and navigate to the mplab-ipe file using the following path.
      1. C:\Program Files (x86)\Microchip\MPLABX\v5.20\mplab\_platform\mplab\_ipe
   4. Right click on 'ipecmd.exe' and click 'Open as path'.
   5. Right Click on 'program-32014-02' and click 'Edit in Notepad'.
   6. On the 4th line, you should find 'SET ipeCmd=...'. Delete the existing address and paste the path you just copied.
      1. NOTE: make sure there is only 1 set of quotation marks. Another set will be pasted with the path.
   7. On the 5th line, you should find 'SET pgmDev='. Change this line to 'SET pgmDev=PK3'. THis is to specify which programming device is being used. In this case, its the 'PICkit™ 3'
   8. Save and close notepad.

<figure><img src="../../.gitbook/assets/image (239).png" alt="" width="563"><figcaption></figcaption></figure>

2. Download the Firmware Update if needed
   1. Navigate to the link [https://www.u-blox.com/en/products/zed-f9p-module?legacy+Current#Documentation-&-resources](https://www.u-blox.com/en/products/zed-f9p-module?legacy+Current#Documentation-&-resources)
   2. Scroll down and click 'Documentation & Resources'
   3. Click 'Firmware Update'.
   4. Download the Latest version and place this file in your 'ROVER6\_A' folder.&#x20;

## Guide

### Initial Programing

1. Plug in the GPS Board to your computer using both the PICkit™3 and a usb cable

<figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

2. Program the board.
   1. Execute ‘program-32014-02.bat’.
   2. After the board is programmed, it will say ‘Board program successful, press any key to exit’.

<figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>

3. Check that the LEDs are illuminated as required
   1. Status LED: Flashing
      1. If it is not illuminated, disconnect everything and place the board in a bag and mark 'BAD'.
   2. Heartbeat LED: Flashing
      1. If the heartbeat is not flashing or illuminated, ensure everything is working as required. If it is , continue. If not place in a bag marked 'BAD'.

<div><figure><img src="../../.gitbook/assets/image (242).png" alt="" width="231"><figcaption><p>Status LED</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (243).png" alt="" width="230"><figcaption><p>Heartbeat LED</p></figcaption></figure></div>

4. Exit the program and unplug everything.



### Firmware Update

1. Open U-Center
2. Plug in the GNSS board to your computer using only a USB-C cable.
3. At the top, click on the upside-down triangle next to the connection symbol and select the corresponding COM Port

<figure><img src="../../.gitbook/assets/image (244).png" alt="" width="563"><figcaption></figcaption></figure>

4. At the top, click Tools>Firmware Update...

<mark style="color:red;">picture here</mark>

5. In the new window, click on the 3 dots next to the 'Firmware image' box.
6. Find the File and click 'Open'.
7. To speed up the update process, a higher baud rate may be used, just ensure that it updated correctly afterwards.
   1. 921600 baud results in \~1 minute
   2. 9600 baud results in \~25 minutes
8. Click 'GO' at the bottom

<figure><img src="../../.gitbook/assets/image (245).png" alt="" width="563"><figcaption></figcaption></figure>

9. Once the update has completed, at the top, go to View>Messages View>UBX>MON>VER
   1. Verify the Version number is 1.51

{% hint style="info" %}
The tree viewer is slightly too skinny. Use the scroll bar at the bottom to slide left and minimize the NMEA branch.
{% endhint %}

<mark style="color:red;">picture here</mark>

10. Power Cycle the board and ensure the status LED doesn't flash.
