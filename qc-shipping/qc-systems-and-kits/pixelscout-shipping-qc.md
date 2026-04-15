---
description: 'Owner: Simon'
---

# PixelScout Shipping QC

## Artifact Locations in Taurus>Production

### Systems & Kits>21282-00 — PixelScout Phase 4

<figure><img src="../../.gitbook/assets/Artifacts.png" alt=""><figcaption></figcaption></figure>

* Calibration Flight Files
  * Ensure files are present
* Verification Flight Files
  * Ensure files are present.
  * Open the file 'quicktile\_0.050m\_rgb\_dewarp.tif' from the '\_out' folder in QGIS and ensure it looks well-stitched.
    * Open QGIS and drag the file into the blank space

{% columns %}
{% column %}
<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>GOOD CALIBRATION</p></figcaption></figure>
{% endcolumn %}

{% column %}
<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>BAD CALIBRATION</p></figcaption></figure>
{% endcolumn %}
{% endcolumns %}

* IMU Calibration Data (tuned and untuned)
* Optional: BPR Files

<details>

<summary>Calibration Files (Preferred but not required)</summary>

<figure><img src="../../.gitbook/assets/Calibration Flight Artifacts (2).png" alt=""><figcaption></figcaption></figure>

| File                                       | Description                                                                                   |
| ------------------------------------------ | --------------------------------------------------------------------------------------------- |
| Session                                    | Session folder of calibration flight                                                          |
| \_cal                                      | Files from calibration tool (includes offsets and new hw\_config)                             |
| \__cal\__&#x6F;ut (optional but preferred) | Quicktile files using calculated offsets to predict how well the verification flight will be. |
| \_out (optional but preferred)             | output of original quicktile before calibration or offsets are applied                        |
| _pix4d (and \_2nd for secondary cam)_      | pix4d files used in the calibration                                                           |
| info                                       | info folder from the camera                                                                   |
| .p4d file                                  | File generated during pix4d processing                                                        |

</details>

<details>

<summary>Verification Files</summary>

<figure><img src="../../.gitbook/assets/Verification Flight Artifacts.png" alt=""><figcaption></figcaption></figure>

| Folder  | Description                                         |
| ------- | --------------------------------------------------- |
| Session | Session folder of verification flight               |
| \_out   | quicktile output                                    |
| info    | info folder from SD card during verification flight |



</details>

<details>

<summary>BPR Files</summary>

<div><figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/BPR Artifacts.png" alt=""><figcaption></figcaption></figure></div>

Two folders per camera, one with the raw pictures, and one with the output files.



bpr\_map.csv is applied to camera to be used for BPR.

</details>

### Sensors>21030-XX — 65R>21030-04

<figure><img src="../../.gitbook/assets/Focus Artifacts.png" alt=""><figcaption></figcaption></figure>

* Focus Session Folder (Same as 65R 21030-02)
  * Optional to take a quick look at a few pictures to see the focus.
* Left, middle, and right target screenshots from the focus app (including right starting with 65R SN 022)&#x20;
  * Only need to make sure all 3 target screenshots are present.
* 'Numbers' file containing max, target, and ending focus scores.
  * Not required but optional to check final score percentages.
    * Above 96% required for middle
    * Above \~75% is required for sides (Prefer closer to 92% but not required)
* Refer to [1-pixelscout-65r-focusing.md](../../technical-instructions/pixel-scout/assembly-steps/1-pixelscout-65r-focusing.md "mention") for more context if desired.

<details>

<summary>What the screenshots look like</summary>

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

</details>

## Checking the Cameras

192.168.42.1 is the address for the Primary Camera

192.168.42.2 is the address for the Secondary Camera



1. plug in power and USB-C on the front of the gimbal
2. Open file explorer and navigate to 192.168.42.1
   1. If prompted, use the following username and password.
      1. Username: sentera
      2. Password: \[leave empty]
   2. Make sure there's no sessions on the camera.
   3. Ensure the hw\_config file has the correct serial number/part number.
   4. Ensure the hw\_config has calibration method set to pix4d and the 'rig\_relatives\_deg' values are set to values other than 0.
   5. Ensure the bpr.csb file exists in the 'info' folder.

<details>

<summary>SD Card Folder</summary>

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Info Folder</summary>

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>hw_config file</summary>

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

</details>

3. Navigate to a web browser and go to 192.168.42.1
   1. Check all the pages to make sure they are agreeable with the following drop down menus.

<details>

<summary>Main</summary>

Primary

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085407.png" alt=""><figcaption></figcaption></figure>

Secondary

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085902.png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>Configuration</summary>

Primary:

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 084925 (1).png" alt=""><figcaption></figcaption></figure>

Secondary:

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085931.png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Image Adjustment</summary>

Primary and Secondary are the same:

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085447.png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary>Diagnostics</summary>

Note: the Serial numbers will be different than pictured

The Connection status in the pictures shows both USB and Ethernet. One or both might say 'Disconnected'

Primary and secondary are the same:

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085647.png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>Update Firmware</summary>

Primary and Secondary are the same

Current firmware version: 4.5.1

<figure><img src="../../.gitbook/assets/Screenshot 2026-03-27 085753.png" alt=""><figcaption></figcaption></figure>

</details>

4. Repeat steps 2 and 3 using IP Address 192.168.42.2



## Checking the Case

Refer to [#final-packing](../../technical-instructions/pixel-scout/calibration-and-verification/case-packing.md#final-packing "mention") for a guide on packing the case. Ensure the case follows this guide correctly.

(in the future, may copy everything to this page.
