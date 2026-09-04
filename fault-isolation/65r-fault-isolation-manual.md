# 65R Fault Isolation Manual



{% embed url="https://forms.zohopublic.com/senterallc/form/PixelScoutFaultIsolation/formperma/bN54SqUa56CyhAohn9bULUPqirxKin4kQN4gVfnykj4" %}

## Common Issues

<details>

<summary>Poor Communication/Random dropouts</summary>

Poor camera communication can result in slower transfer speeds, random dropouts, and USB connectivity errors. Here are a few steps to take to diagnose it

1. Open a command prompt and type the following:

```
ping 192.168.42.1
```

{% hint style="info" %}
You can add ' -t' to the end of it to run it continuously so you can monitor the connection while working with the camera. To stop, hit ctrl+c.
{% endhint %}

2. Watch for the response times. They should be <=1ms. If they are consistently higher than 1 ms, the computer is trying to connect with another device on the John Deere network that uses the same IP Address as the cameras. A good fix is to connect to Sentera Guest WIFI.
3. If you are getting errors, hit windows+r, type 'ncpa.cpl' and click 'OK'.
4. If there are only 2 things on this page, it is likely that the computer is not seeing the device.

</details>

<details>

<summary>One side of picture out of focus</summary>

65R imager boards have been showing up with tilted imagers on the imager board. This causes on side of the frame to be out of focus compared to the other side.



Replace Imager board.



Possibly apply kapton tape to low side to level the imager.

</details>

<details>

<summary>Red stripped image, then black</summary>

During focusing, the first image taken was a weird, red, stripped image and every image after that was black.

<div><figure><img src="../.gitbook/assets/IMG_0001 (1).jpg" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/IMG_0002 (1).jpg" alt="" width="375"><figcaption></figcaption></figure></div>

This camera was fixed by replacing the imager board.

</details>

<details>

<summary>Failed BPR (Bad Pixel Replacement)</summary>

1. As of 7/15/2026 we are switching the mount for the 65R.&#x20;
2. Send images to Zach Thorson to confirm
3. Switch out mount and try BPR again&#x20;
4. Send Images to Zach again if it passes BPR

</details>

<details>

<summary>No lights on the camera </summary>

The imager board controlls the lights on the 65R. It will not let you start a session without the lights working properly



1. Switch out the imager board and see if the lights come back.&#x20;
2. Message help-embedded or Alex Stephens to see if the board can be fixed.&#x20;

</details>

