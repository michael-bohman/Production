---
description: '21283-00 - Owner: Isaac'
---

# 🚧 21283-00 -- Camera Pod Assembly

<figure><img src="../../../.gitbook/assets/build_flow_camera_pod_assembly.drawio (1).png" alt="" width="332"><figcaption></figcaption></figure>

## Drawing:

{% content-ref url="../../../space-and-general/drawings.md#pixelscout-v4-camera-pod-greater-than-21283" %}
[#pixelscout-v4-camera-pod-greater-than-21283](../../../space-and-general/drawings.md#pixelscout-v4-camera-pod-greater-than-21283)
{% endcontent-ref %}

## Notes:

These instructions end with two separate components, the back with the rangefinders and the front with the cameras. These halves will be joined in a later instruction set.

## Prep:

| Loctite        | Small Heat Shrink | Heat gun |
| -------------- | ----------------- | -------- |
| Wire-strippers |                   |          |

## Guide:

{% stepper %}
{% step %}
### Rangefinders

* If not done already, prep the rangefinders by cutting the wires and applying a small \~1" strip of heat shrink to the open ends.
* Insert the rangefinders into the rear housing. Secure using 4 screws (<mark style="color:yellow;">91698A302 M3x6 Flt Hd Blk</mark>) each and Loctite.

<div><figure><img src="../../../.gitbook/assets/IMG_7859.jpg" alt="" width="563"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/IMG_7860.jpg" alt="" width="563"><figcaption></figcaption></figure></div>
{% endstep %}

{% step %}
### Cameras

* Assign primary and secondary cameras by serial number.
  1. The cameras used should be in succession.&#x20;
  2. The LOWER serial number camera will be designated as the PRIMARY.

<figure><img src="../../../.gitbook/assets/IMG_7861 mod.jpg" alt="" width="563"><figcaption></figcaption></figure>

* Attach the Cameras to the camera pod assembly in their designated mounts. Secure using 4 screws (<mark style="color:yellow;">93085A015 2-56x.188" Flat Head from #22 of 6X screw bin</mark>) EACH and Loctite.
  1. Hold the cameras in place and insert the screws about halfway with Loctite before going back and tightening all of them.
  2.  It may be easiest to screw in the back ones first.

      <figure><img src="../../../.gitbook/assets/IMG_7655.jpg" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Micro-Coax Cables

* Remove the back covers of each camera using 7 screws (or 3 if progressing from 21030-04 — 65R page) on the rear.

<figure><img src="../../../.gitbook/assets/IMG_7862.jpg" alt="" width="375"><figcaption></figcaption></figure>

* Attach the PSDK micro coax cable to the micro-USB breakout board.

<figure><img src="../../../.gitbook/assets/IMG_7657 (1).jpg" alt="" width="375"><figcaption></figcaption></figure>

* Route the cable to the correct corner (relative to the micro-coax breakout board) and place the cover back on, ensuring the cable stays in place and is not pinched.
  1. Primary will go to the close corner (shown)
  2. Secondary will go to the far corner

<div><figure><img src="../../../.gitbook/assets/IMG_7864.jpg" alt="" width="563"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/IMG_7865.jpg" alt="" width="563"><figcaption></figcaption></figure></div>

| Primary                                                                           | Secondary                                                                         |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| <img src="../../../.gitbook/assets/IMG_7656 (2).jpg" alt="" data-size="original"> | <img src="../../../.gitbook/assets/IMG_7658 (1).jpg" alt="" data-size="original"> |

* Re-apply Loctite to the screws and secure the cover.
{% endstep %}
{% endstepper %}

## Next Step:

If Gimbal is not completed:

{% content-ref url="21283-00-camera-pod-assembly.md" %}
[21283-00-camera-pod-assembly.md](21283-00-camera-pod-assembly.md)
{% endcontent-ref %}

If Gimbal is already completed:

{% content-ref url="21282-00-sensor-assembly.md" %}
[21282-00-sensor-assembly.md](21282-00-sensor-assembly.md)
{% endcontent-ref %}
