# F9P Board Programming

## Required Equipment/Materials

* TTL Cable
* 12 V AC Power Adapter (Anderson Power Pole connector)
* GPS board programming adapter cable



## Notes

The file uploaded to the antenna GNSS board is the same for the PixelScout system as it is for the RTK/PPK system.



## Prep

1. Download the U-Center 25.06 software using the Software Installation Guide Page.

[#u-center-v25.06](../../../space-and-general/software-installation-guide.md#u-center-v25.06 "mention")

2. Download the Bin file from Taurus to somewhere on your laptop.
   1. Taurus>Data>Part Database (things we sell)>SW-32026-01 — Zed F9P>Firmware
   2. Filename: UBX\_F9\_100\_HPG151\_ZED\_F9P.6c43b30ccfed539322eccedfb96ad933.bin
   3. Note the '151' is the version number of the firmware.

## Guide

1. Open U-Center
2. Plug in everything
3. At the top, click on the upside-down triangle next to the connection symbol
4. Select the corresponding COM Port
5. Ensure the box at the bottom shows a green symbol and displays a baud rate
   1. If not, refer to the Fault Isolation Manual
6. At the top, click Tools>Firmware Update...
7. In the new window, click on the 3 dots next to the 'Firmware image' box.
8. Find the File and click 'Open'.
9. To speed up the update process, a higher baud rate may be used, just ensure that it updated correctly afterwards.
   1. 921600 baud results in \~1 minute
   2. 9600 baud results in \~25 minutes
10. Click 'GO' at the bottom
11. Once the update has completed, at the top, go to View>Messages View>UBX>MON>VER
    1. Verify the Version number is 1.51

{% hint style="info" %}
The tree viewer is slightly too skinny. Use the scroll bar at the bottom to slide left and minimize the NMEA branch.
{% endhint %}
