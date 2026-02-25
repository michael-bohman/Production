# 6X Fault Isolation Manual

## Common Issues (Try First)

<details>

<summary>Not Taking Pictures </summary>

1. Reconfigure camera&#x20;
   1. Sometimes when taking photos the 6X just needs a refresh. Keep it on Sentera OEM GPS

</details>

<details>

<summary>No Connection to the webpage</summary>

1. Confirm all the switches on the baseboard are in the correct position
2. Power cycle camera&#x20;
3. Switch cables&#x20;
4. In the start menu, search <mark style="color:blue;">**RUN**</mark>
5. In the search box type in <mark style="color:blue;">**ncpa.cpl**</mark>

<figure><img src="../.gitbook/assets/image (55).png" alt="" width="429"><figcaption></figcaption></figure>

6. Click enter, after a few seconds another window will appear&#x20;
7. With power and usb connected, you should see 2 ethernets appear. This will tell you if the camera is reading any network. If no network appears, the webpage will not show up

<figure><img src="../.gitbook/assets/image (54).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

## Common Error Codes&#x20;

<details>

<summary>Pixel Alignment Error (Some Pictures are dark)</summary>

* After running through pixel alignment program the results have some completely blacked out photos

<figure><img src="../.gitbook/assets/image (56).png" alt="" width="563"><figcaption></figcaption></figure>

* Look at the lens number at the bottom of the image. Then check the focus session and confirm the images are blacked out as well&#x20;

<figure><img src="../.gitbook/assets/image (57).png" alt="" width="563"><figcaption></figcaption></figure>

This is a common issue that can happen when the autoexposure does not catch up when taking the focus images.&#x20;

***

Solution: Retake the focus images

1. Once focus images are retaken, load the new Focus session into your SN folder for pixel alignment. Label the old focus session something else, so the sessions don't get mixed up.&#x20;

{% hint style="info" %}
You do not need to retake CAL photos. Just retake Focus photos
{% endhint %}

<figure><img src="../.gitbook/assets/image (58).png" alt="" width="527"><figcaption></figcaption></figure>

2. Load in the CAL, New Focus

</details>
