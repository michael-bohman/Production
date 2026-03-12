---
description: >-
  Simon is working on this and will fill more of it out later. These are just
  some quick notes
---

# PixelScout Shipping QC



## Artifact Locations in Taurus>Production

### Systems & Kits>21282-00 — PixelScout Phase 4

<figure><img src="../../.gitbook/assets/Artifacts.png" alt=""><figcaption></figcaption></figure>

* Calibration Flight Files
  * Ensure files are present
* Verification Flight Files
  * Ensure files are present.
  * Open .tif file from '\_out' folder in QGIS and ensure it looks well-stitched.
* IMU Calibration Data (tuned and untuned)
* Optional: BPR Files

<details>

<summary>Calibration Flight Files</summary>

<figure><img src="../../.gitbook/assets/Calibration Flight Artifacts (1).png" alt=""><figcaption></figcaption></figure>

| Folder/File                         | Description                                                                        |
| ----------------------------------- | ---------------------------------------------------------------------------------- |
| Session                             | Session from calibration flight                                                    |
| \_cal                               | output from calibration software with new hw\_config, offsets, quicktile and stats |
| \_cal\_out                          | quicktile using alignment offsets calculated from calibration software             |
| \_out (optional)                    | quicktile using un-aligned settings as a baseline                                  |
| \_pix4d (2nd for secondary cameras) | pix4d files generated during computation                                           |
| info                                | info folder from camera SD card during calibration flight                          |
| .p4d file                           | pix4d session file                                                                 |

</details>

<details>

<summary>Verification Flight Files</summary>

<figure><img src="../../.gitbook/assets/Verification Flight Artifacts.png" alt=""><figcaption></figcaption></figure>

| Folder  | Description                                         |
| ------- | --------------------------------------------------- |
| Session | Session folder of verification flight               |
| \_out   | quicktile output                                    |
| info    | info folder from SD card during verification flight |



</details>

<details>

<summary>BPR Files</summary>

<figure><img src="../../.gitbook/assets/BPR Artifacts.png" alt=""><figcaption></figcaption></figure>

bpr\_map.csv is applied to camera to be used for BPR.

</details>

### Sensors>21030-XX — 65R>21030-04

<figure><img src="../../.gitbook/assets/Focus Artifacts.png" alt=""><figcaption></figcaption></figure>

* Focus Session Folder (Same as 65R 21030-02)
* Left, middle, and right target screenshots from the focus app
* 'Numbers' file containing max, target, and ending focus scores.
