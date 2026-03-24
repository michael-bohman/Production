---
description: Stage 2 in the 6X process
---

# 6X Programming

## Equipment Needed

<table data-header-hidden data-full-width="true"><thead><tr><th align="center"></th><th align="center"></th></tr></thead><tbody><tr><td align="center">12v 6x power supply </td><td align="center">Tweezers</td></tr><tr><td align="center">USB-C Cable </td><td align="center">Scissors</td></tr><tr><td align="center">Printed sensor label with serial number and part number </td><td align="center">Laptop</td></tr></tbody></table>

## Guide

### Computer SD Card

1. Open a brand new SD Card and insert into your computer&#x20;
2. Follow the path listed below to find the Firmware-sdcard folder
   1. \as-taurus.jdnet.deere.com\Production\Technical Packages\6X SENSOR\IN PROGRESS\6X SENSOR - Technical Data Package - 251007\6X SENSOR - PROGRAMMING\6X-21214\_Programming\firmware - sdcard
3. Copy all 3 files into the SD Card (BOOT.bin, image.ub, uEnv)
4. Eject SD card and insert into camera&#x20;

### Camera Firmware Update

1. On the Camera, set the dip switches on the imager baseboard CCA to the following below

<figure><img src="../../.gitbook/assets/Dip Switch setting 1.png" alt=""><figcaption></figcaption></figure>

6. Power on the camera and connect USB-C cable&#x20;
7. Open the camera website 192.168.42.1
8. Select the update firmware tab&#x20;
9. Drag and drop the file from taurus into the camera to update&#x20;
   1. \as-taurus.jdnet.deere.com\Production\Technical Packages\6X SENSOR\IN PROGRESS\6X SENSOR - Technical Data Package - 251007\6X SENSOR - PROGRAMMING\6X-21214\_Programming\firmware - factory update
10. Once update is complete, power off camera and remove SD card&#x20;

{% hint style="info" %}
When the update is complete, the firmware will not refresh and show the correct numbers until the Confirmation check&#x20;
{% endhint %}

### Firmware Folder

1. Insert SD card into computer&#x20;
2. Delete all 3 files on the SD card&#x20;
3. Copy the firmware folder from Taurus onto the SD Card (confirm build number for correct files)
   1. \as-taurus.jdnet.deere.com\Production\Technical Packages\6X SENSOR\IN PROGRESS\6X SENSOR - Technical Data Package - 251007\6X SENSOR - PROGRAMMING\6X-21214\_Programming\configs\21214-02
4. Open the hw\_config.yaml and update the serial number for the camera you have&#x20;
5. Cut out label and stick onto the camera
   1.

       <figure><img src="../../.gitbook/assets/image (2).png" alt="" width="292"><figcaption></figcaption></figure>
6. Eject SD card and insert into camera&#x20;

### Confirmation Check

1. On the Camera, set the dip switches on the imager baseboard CCA to the following below

<figure><img src="../../.gitbook/assets/Dip Switch setting 2.png" alt=""><figcaption></figcaption></figure>

2. Power on the camera and connect USB-C cable&#x20;
3. Open the camera website 192.168.42.1
4. Confirm firmware is up to date and showing the right numbers&#x20;
5. Confirm Diagnostics is showing the correct Part number and serial number for your camera&#x20;
6. Open the Home tab&#x20;
7. Find the Session button and rename to "Prog Test Session", Click Start Session
8. Wait a few sessions and click Capture Image
9. Navigate to file explorer  \\\192.168.42.1&#x20;
10. Confirm photos have been taken&#x20;



### After Programming Back Half Assembly

1. Remove the screws securing the fan in place.
2. Fit the rear cover over the back of the sensor
3. The cover should lightly clip into place

> ![](<../../.gitbook/assets/image (20).png>)    ![](<../../.gitbook/assets/image (21).png>)

2. Secure rear cover and fan using the screws removed in the last step
   1. Secure rear cover to heatsink with (Item 40)&#x20;
   2. Secure rear cover to heatsink on left side of the sensor with one (Item 28)
   3.

       <figure><img src="../../.gitbook/assets/Back cover.jpg" alt=""><figcaption></figcaption></figure>

