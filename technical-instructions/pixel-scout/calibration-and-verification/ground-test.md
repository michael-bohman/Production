---
description: 'Owner: Isaac'
---

# ✅ Ground Test

## Materials/Equipment Needed

| PixelScout V4 Gimbal          | PixelScout V4 Antenna    | PixelScout V4 Base Station kit |
| ----------------------------- | ------------------------ | ------------------------------ |
| PixelScout V4 Production Case | iPad with Emlid Flow App |                                |
|                               |                          |                                |

## Notes

This instruction set assumes the reader is already familiar with setting up and flying a DJI drone and may not give enough context for someone to learn how to do so.

Do this outside and in an open area to ensure the system can reach an RTK FIX solution.



## Prep

1. Charge Batteries
   1. iPad
   2. Drone Batteries
   3. Hand Controller Battery

## Setup

### Base Station Setup (do first)

This is so that the base station has time to reach RTK status before you are ready to fly.

1. Refer to the 'Field Setup' page for this. [field-setup.md](../emlid-base-station/field-setup.md "mention")

<figure><img src="../../../.gitbook/assets/IMG_8070 (1).jpeg" alt="" width="375"><figcaption></figcaption></figure>

### Drone Setup

1. Attach the gimbal to the drone using the Skyport connection (push up and twist).

<figure><img src="../../../.gitbook/assets/IMG_9048.jpg" alt="" width="375"><figcaption></figcaption></figure>

2. Clip the antenna to the legs of the drone with the lights facing forward and the sticker saying 'This side faces rear' facing rear. Tilt the antenna down and aft.

<figure><img src="../../../.gitbook/assets/IMG_8073.jpeg" alt="" width="563"><figcaption></figcaption></figure>

3. Ensure the clips on the antenna are fully clipped with the lip in the slot, not just clipped around the leg.

{% columns %}
{% column %}
<figure><img src="../../../.gitbook/assets/IMG_8071 (1).jpeg" alt=""><figcaption></figcaption></figure>

<mark style="color:red;">BAD</mark>
{% endcolumn %}

{% column %}
<figure><img src="../../../.gitbook/assets/IMG_8072.jpeg" alt=""><figcaption></figcaption></figure>

<mark style="color:$success;">GOOD</mark>
{% endcolumn %}
{% endcolumns %}

4. Plug in the antenna to the back of the gimbal and ensure it is secure.

<figure><img src="../../../.gitbook/assets/IMG_9049.jpg" alt="" width="375"><figcaption></figcaption></figure>

5. Set up all the regular things of a normal drone flight (arms, etc.)

<figure><img src="../../../.gitbook/assets/IMG_9050.jpg" alt="" width="375"><figcaption></figcaption></figure>

6. Turn on the drone and hand controller.



## Checks

If anything is not as expected, refer to the fault isolation manual for a guide on how to fix it.

[pixelscout-fault-isolation.md](../../../fault-isolation/pixelscout-fault-isolation.md "mention")

1. The antenna lights should show 4 green lights with one red light NOT illuminated.
   1. If the red light is illuminated, refer to the fault isolation manual

<figure><img src="../../../.gitbook/assets/IMG_8075.jpeg" alt="" width="563"><figcaption></figcaption></figure>

2. Both cameras should start sessions (turn green)

<figure><img src="../../../.gitbook/assets/IMG_8076.jpeg" alt="" width="563"><figcaption></figcaption></figure>
