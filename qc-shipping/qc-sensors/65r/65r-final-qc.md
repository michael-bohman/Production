---
description: >-
  Once 65R has gone through flight test, check-in and the pre-shipment setup is
  complete, then the Final QC can occur.
---

# 65R Final QC

{% hint style="danger" %}
This step should be completed by a different person that did the build and pre-shipment set-up. During Final QC, your job is to confirm everything is perfect. The package should not be shipped out with any issues.&#x20;
{% endhint %}

## Camera Check&#x20;

1. Power on the 65R camera and go to website "192.168.42.1". If you are required to enter in credentials, the username is "sentera" and leave the password blank.
2. Confirm the following
   1. Firmware is up to date&#x20;
   2. Correct Configuration is set use the following to confirm the correct config according to the SOS part number that is being shipped.&#x20;
      1. 21931-00, 21931-01, 21931-12, 21931-13 M300/M350 --> DJI skyport, Gimbaled
      2. 21931-02, 21931-03, 21931-14, 21931-15 Freefly Astro --> Freefly Astro Gimbal
      3. 21931-04, 21931-05, 21931-16, 21931-17 IF800 --> IF800, Inspired Flight Gimbal
      4. 21931-06, 21931-07, 21931-18, 21931-19 IF1200 --> IF1200A, Inspired Flight Gimbal
      5. 21931-08, 21931-09, 21931-20, 21931-21 OEM --> Sentera GPS, OEM
      6. 21931-10, 21931-11 Gremsy --> MAVLink-v2, Gremsy Hyper Quick
   3. Diagnostics is the same P/N and S/N as the camera
3. Go to File explorer and type in \\\192.168.42.1
   1. "\\\192.168.42.1\data\snapshots" is empty&#x20;
   2. "\\\192.168.42.1\sdcard\info\hw\_config.yaml" has the correct S/N. Make sure this S/N matches the 6x's SOS build and the label on the outside of the sensor.
4. Visual Check&#x20;
   1. Sticker is clean&#x20;
   2. Screws attaching the sensor to the gimbal are at the correct torque spec (15 inch-oz) and none of them are missing. This includes all three philips head screws and the shoulder screw.
   3. SD card is secured&#x20;
   4. The lens is clean and do not have any smudges or fingerprints on them
5. Taurus Check&#x20;
   1. Using File Explorer, navigate to "\\\as-taurus.jdnet.deere.com\Production\Sensors\\". Find and open the folder for the specific part number and serial number of the Sensor being QC'd.
   2. Data folder contains the Focus and Flight Test. It is also acceptable to have a folder named BPR with no images. Check Focus and Flight Test imagery.
   3. SDcard includes Firmware, info, and System Volume Information
   4. CheckinDoc is in folder, Click into Checkin and read through it

<figure><img src="../../../.gitbook/assets/Camera Check in Taurus.png" alt=""><figcaption></figcaption></figure>

## &#x20;Paper Information Check

1. On the packing list, confirm the following
   1. Item QTY being shipped matches
   2. All items are included in the shipment
2. On the Shipping Label, confirm the following via the Sales Order
   1. Address is correct&#x20;
   2. Names are spelled correctly&#x20;
   3. Tracking order is the same

## Accessories Check&#x20;

{% hint style="danger" %}
Remove the items out of the case to check them. &#x20;
{% endhint %}

1. There should be 2 Small Red Lined bags, First bag includes (Bag A)
   1. 2 gray USB-A to C Adapters&#x20;
   2. 1 black USB-C to C @ 90 degree Adapter

<figure><img src="../../../.gitbook/assets/20260212_074732 (1).jpg" alt="" width="563"><figcaption></figcaption></figure>

3. Confirm case looks like the image below(pic needed)
4. Put the Sentera sticker in the case

## Pack the Shipment

1. Get a blue Sentera box and tape the bottom
2. Confirm sticker is in the 6X case&#x20;
3. Do a last visual check and then close the case&#x20;
4. Put the case into the plastic bag provided
5. Put the packing list in the box on top of the case&#x20;
6. Put the case in the box (no bubble wrap needed)
7. Tape the top of the box&#x20;
8. Stick on the label&#x20;
9. Put package in shipping location&#x20;
