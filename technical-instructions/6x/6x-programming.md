---
description: Stage 2 in the 6X process
---

# 6X Programming

## Equipment Needed

* 12v 6x power supply&#x20;
* USB-C Cable&#x20;
* Laptop&#x20;

## Computer SD Card

1. Open a brand new SD Card and insert into your computer&#x20;
2. Follow the path listed below to find the Firmware-sdcard folder
   1. \as-taurus.jdnet.deere.com\Production\Technical Packages\6X SENSOR\IN PROGRESS\6X SENSOR - Technical Data Package - 251007\6X SENSOR - PROGRAMMING\6X-21214\_Programming\firmware - sdcard
3. Copy all 3 files into the SD Card (BOOT.bin, image.ub, uEnv)
4. Eject SD card and insert into camera&#x20;

## Camera Firmware Update

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

## Firmware Folder

1. Insert SD card into computer&#x20;
2. Delete all 3 files on the SD card&#x20;
3. Copy the firmware folder from Taurus onto the SD Card (confirm build number for correct files)
   1. \as-taurus.jdnet.deere.com\Production\Technical Packages\6X SENSOR\IN PROGRESS\6X SENSOR - Technical Data Package - 251007\6X SENSOR - PROGRAMMING\6X-21214\_Programming\configs\21214-02
4. Open the hw\_config.yaml and update the serial number for the camera you have&#x20;
5. Eject SD card and insert into camera&#x20;

## Confirmation Check

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
