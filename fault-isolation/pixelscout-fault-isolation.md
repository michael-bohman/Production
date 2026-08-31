---
description: 'Owner: Isaac'
---

# PixelScout Fault Isolation



{% embed url="https://forms.zohopublic.com/senterallc/form/PixelScoutFaultIsolation/formperma/bN54SqUa56CyhAohn9bULUPqirxKin4kQN4gVfnykj4" %}

## Gimbal

<details>

<summary>Only one session starts</summary>

<figure><img src="../.gitbook/assets/IMG_7912.JPG" alt="" width="375"><figcaption></figcaption></figure>

This may happen randomly and just needs a restart or two. Otherwise the system may have some outdated softwares on them

1. Restart the camera a max of 2 times to try to fix it.
2. Check the software/firmware versions on all the components (cameras, boards, etc.)

</details>

<details>

<summary>Only takes a few pictures and they're all corrupted</summary>

After flying, one camera's sessions only has 4 or so pictures and none of them can be opened because they say they are corrupted.



This may be a rare occurence: e.g. SN 118 did it a only a few times during 40 power cycles.



New NVME is best guess for fix.

</details>

<details>

<summary>GPS Jumps to 0,0 for a bit</summary>

During calibration, pix4d shows a picture or few at null island (0 lattitude, 0 longitude).

Dots in flight plan may stray from the line as well.

<figure><img src="../.gitbook/assets/Screenshot 2026-05-15 213120.png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2026-05-15 213259.png" alt="" width="375"><figcaption></figcaption></figure>



New SBG Board fixed the issue.



This was most likely caused by the vibration of the SBG board. This is why we enabled Vibration EKF and summary logging in the SBG configuration.

</details>

## Antenna

<details>

<summary>Flashing Antenna Lights</summary>

<figure><img src="../.gitbook/assets/Video Project.gif" alt=""><figcaption></figcaption></figure>



1. Check that the base station is using 1 Hz for all the RTCM3 message frequencies.

</details>

<details>

<summary>U-Center box doesn't show green symbol/baud rate</summary>

Check the baud rate used for communication.

1. At the top, click Receiver>Autobauding

</details>

