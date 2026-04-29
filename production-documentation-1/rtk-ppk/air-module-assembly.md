---
description: Air Module 21077
---

# Air Module Assembly

Refer to this document until gitbook is properly updated.&#x20;

{% file src="../../.gitbook/assets/RTK PPK Production Guide - 2026_01_20.pdf" %}

## Equipment Needed&#x20;

|                   |                   |                   |
| ----------------- | ----------------- | ----------------- |
| Paper towels&#xD; | Mixing Tray       | Loctite           |
| Scissors          | Stirring Sticks   | Ruler             |
| Araldite          | Isopropyl Alcohol | Soldering Station |
| White 28 AWG Wire | JST Chrimp        |                   |

## Notes&#x20;

The P900 and GPS Board programming need to be completed before assembly. Refer to [p900-radio-programming.md](p900-radio-programming.md "mention") and [z9p-gps-board-programming.md](z9p-gps-board-programming.md "mention") before continuing assembly.

## Drawing&#x20;

{% content-ref url="../../space-and-general/drawings.md#rtk-ppk-air-module-greater-than-21077" %}
[#rtk-ppk-air-module-greater-than-21077](../../space-and-general/drawings.md#rtk-ppk-air-module-greater-than-21077)
{% endcontent-ref %}

## Guide

1. Solder a 4’ white wire to the pin on the back of the connector of the GPS board.
   1. Measure and cut 6” of white 28 AWG wire.&#x20;
   2. Strip one end and crimp a JST connector onto it&#x20;
   3.

       <figure><img src="../../.gitbook/assets/image (130).png" alt="" width="459"><figcaption></figcaption></figure>
   4. Insert the wire into pin 7 of the 11 pin connector&#x20;
   5.

       <figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>
   6. On the other end solder the wire to pin #8 of the 9-pin JST connector marked ‘IN’ on the GPS      \
      board.
   7.

       <figure><img src="../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>
2. Install diffuser to enclosure using with screw <mark style="color:yellow;">(Item #11 91772A065)</mark> and Loctite. Torque to 20 in-oz.

<figure><img src="../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

3. Install USB-C Breakout Board
   1. Remove nut and lock washer from USB-C breakout board MCX connector. Discard lock washer
   2. Place board into position in enclosure. Loosely fasten nut on MCX connector. Install 2 screws <mark style="color:yellow;">(Item #11 91772A065)</mark> with Loctite. Torque to 20 in-oz.
   3.

       <figure><img src="../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>
   4. Tighten nut with wrench
4. Install GPS board
   1. Plug the 8-pin JST connector into the ETH2 port of the GPS board
   2.

       <figure><img src="../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>
   3. Remove nut and lock washer from SMA connector on GPS board. DO NOT DISCARD.
   4. Place GPS board into enclosure. GPS board should be oriented such that the LED aligns with the diffuser and all 4 screw holes are aligned with those on the enclosure.
   5. Replace lock washer and nut on SMA connector. Tighten nut with wrench. Double check the screw holes are still aligned.<br>

{% columns %}
{% column width="50%" %}
<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column width="50%" %}
<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

5. Install USB-A breckout board
   1. Install USB-A breakout board to enclosure using 2 screws <mark style="color:yellow;">(Item #11 91772A065)</mark> and Loctite. Torque to 20 in-oz.
6. &#x20;Install radio board
   1. Carefully place 4 spacers <mark style="color:yellow;">(Item #9 94639A703)</mark> on GPS board above screw holes.
   2. &#x20;![](<../../.gitbook/assets/image (139).png>)
   3. Install radio board on top of GPS board making sure to align the connector on the back\\
   4. Install 4 screws <mark style="color:yellow;">(Item #10 91772A080)</mark> through radio board, spacers, and GPS board with Loctite. Torque to 40 in-oz
   5.

       <figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>
7. Connect the cables and route as shown below
   1. Connect USB-C and USB-A breakout boards&#x20;
   2. Install the coax cable to the radio and USB-C boards&#x20;

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

9. Prepare and install cover
   1. Cut 2 small squares from the foam pad and install them on the raised circles of the cover
   2. Install the cover to the enclosure using 4 screws <mark style="color:yellow;">(Item #12 93085A017)</mark> and Loctite. Torque to 40 in-oz

{% columns %}
{% column %}
<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

10. Install Antenna
    1. Install the O-ring <mark style="color:yellow;">(Item 14 2418T126)</mark> into the channel on top of the enclosure
    2. Install the helical antenna to the SMA connector on top of the enclosure. Tighten by hand until snug
11. Install 4 captive thumb screws <mark style="color:yellow;">(Item #13 M0171-SS)</mark> into threaded holes of the cover
12. Clean empty side of enclosure with alcohol. Apply Radio Net ID sticker with corresponding number as shown

{% columns %}
{% column %}
<figure><img src="../../.gitbook/assets/Screenshot 2026-04-28 134334.png" alt=""><figcaption></figcaption></figure>


{% endcolumn %}

{% column %}
Change numbers to the correct serial numbers

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}
{% endcolumns %}
