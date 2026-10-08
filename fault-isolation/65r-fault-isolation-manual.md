# 65R Fault Isolation Manual

## Report Issues

{% hint style="danger" %}
Do not report issues for RMA's. You can add an expandable below in "Known Issues".&#x20;
{% endhint %}

{% embed url="https://forms.zohopublic.com/senterallc/form/65Rfaultisolation1/formperma/CJcEYZErSP_-w5Tm83R5N2hj8tm-IVSsH5eRuiAEZe4" %}

## Known Issues

Adding a new issue:

* Add expandable and summarize a title&#x20;
* Add description of how it happened
* Add possible soulution or troubleshooting&#x20;
* Slack [Amanda Janssen](https://sentera.slack.com/archives/D06TB8LH7B2) to update form

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

1. Enter into asset tracker and give to Alex Stephens
2. You will likely need to replace imager board

</details>

<details>

<summary>Failed BPR (Bad Pixel Replacement)</summary>

1. Rotate the lens mount, retake pictures and run map again.&#x20;

</details>

<details>

<summary>No lights on the camera </summary>

The imager board controlls the lights on the 65R. It will not let you start a session without the lights working properly



* Enter into asset tracker and give to Alex Stephens
* You will likely need to replace imager board

</details>

<details>

<summary>When on a gimbal the camera slowly rotates to one side </summary>

This is caused by the fan. It vibrates and the camera rotates because of it.&#x20;

1. Replace fan&#x20;
2. Confirm issue does not happen before shipping with multiple start ups&#x20;

</details>

<details>

<summary>Factory Firmware Update Failed</summary>

When booting off the SD card for the first time and trying to do a factory update, it fails.&#x20;

1. Unplug power, reinsert SD card and try again&#x20;
2. If unsuccessful, reapply boot files to the SD card and try update again

</details>

<details>

<summary>Snapshots folder disappeared</summary>

When deleting all sessions from 65R the snapshots folder disappears after restart.

1. This is an issue being looked at, but does not prevent shipping. Once a new session starts the snapshots folder will come back.&#x20;

</details>

<details>

<summary>Unable to start a session</summary>

When trying to start a session, the 192.168.42.1 homepage website errors out with a red screen and the camera displays flashing red lights.

<p align="center">or </p>

When trying to start a session, the 192.168.42.1 homepage website never loads the "capture image" button. The baseboard doesn't consistently flash the green and orange lights.&#x20;



This is usually the imager board. Look at the logs and see if any of the following messages are seen.&#x20;

* Bad imager initialization
* Unable to initialize imager! Missing Start of Frame!
* GMAX is missing



1. Enter into asset tracker and give to Alex Stephens
2. You will likely need to replace imager board

</details>

