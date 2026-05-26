---
description: 'Owner: Simon'
---

# 📷 3-B F9P Board Programming

Things Needed:

* Plugging Everything in
* Select the COM port
* Select the firmware update file

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
   1. Taurus>Data>Part Database (things we sell)>SW-33026-01 — Zed F9P>Firmware
   2. Filename: UBX\_F9\_100\_HPG151\_ZED\_F9P.6c43b30ccfed539322eccedfb96ad933.bin
   3. Note the '151' is the version number of the firmware.
   4. Or use the following download link (Confirm the version is the latest before using)

{% file src="../../../.gitbook/assets/UBX_F9_100_HPG151_ZED_F9P.6c43b30ccfed539322eccedfb96ad933.bin" %}

## Guide

1. Open U-Center
2. Plug in everything

<mark style="color:red;">Picture Here</mark>

2. At the top, click on the upside-down triangle next to the connection symbol
3. Select the corresponding COM Port

<mark style="color:red;">Picture here</mark>

4. Ensure the box at the bottom shows a green symbol and displays a baud rate
   1. If not, refer to the Fault Isolation Manual

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163236.png" alt=""><figcaption></figcaption></figure>

5. At the top, click Tools>Firmware Update...

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163252.png" alt="" width="375"><figcaption></figcaption></figure>

6. In the new window, click on the 3 dots next to the 'Firmware image' box.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163516.png" alt="" width="375"><figcaption></figcaption></figure>

7. Find the File and click 'Open'.

<mark style="color:$danger;">Picture Here</mark>

8. To speed up the update process, a higher baud rate may be used, just ensure that it updated correctly afterwards.
   1. 921600 baud results in \~1 minute
   2. 9600 baud results in \~25 minutes

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163516_2.png" alt="" width="375"><figcaption></figcaption></figure>

9. Uncheck all 4 options next to the baud rate.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163516_3.png" alt="" width="375"><figcaption></figcaption></figure>

10. Click 'GO' at the bottom

<figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 163516_4.png" alt="" width="375"><figcaption></figcaption></figure>

8. Once the update has completed, at the top, go to View>Messages View>UBX>MON>VER
   1. Verify the Version number is 1.51

{% hint style="info" %}
The tree viewer is slightly too skinny. Use the scroll bar at the bottom to slide left and minimize the NMEA branch.
{% endhint %}

<div><figure><img src="../../../.gitbook/assets/Screenshot 2026-05-25 154001 (1).png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2026-05-26 162730 (1).png" alt="" width="323"><figcaption></figcaption></figure></div>
