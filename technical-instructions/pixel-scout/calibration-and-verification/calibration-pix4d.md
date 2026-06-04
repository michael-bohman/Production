---
description: 'Owner: Simon'
---

# 🚧 Calibration (Pix4d)

Things to add:

* quality report checks.
* Setup process
* Applying to camera

## Notes

* THIS IS A LONG PROCESS. If using the embedded2 desktop, plan for about 2 hours. DO NOT use the regular John Deere laptops as it will take longer than all day.

## Setup

1. Copy the session and info folder into a 'Primary' and 'Secondary' folder inside a serial number folder.
2. Download the programs required. They are in taurus in the following path.
   1. taurus>asdf
3. If logged out, use the shared pix4d login on embedded2

{% hint style="info" %}
NOTE: only use a new license if you plan on using the pix4d program often. There are limited licenses. Use Embedded2 if possible.
{% endhint %}



## Starting Quicktile (Preferred but Optional)

1. Open the quicktile program
2. Select each session folder (primary and secondary) as an input.
3. The output should be named the session plus '\_out' at the end.
4. Run the quicktiler.
5. When its done running. go to the out folder and find the .tif (photo icon).
6. Open QGIS and drag the .tif into it to see the pre-calibration stitched view. (NOT REQUIRED)



## Pix4d

1. Open two instances of pix4d, one for the primary and one for the secondary camera.
2. Create a new project named the same as the session with '\_pix4d' at the end
   1. For the secondary camera, also add '\_2nd' at the end.
   2. Save the project to the 'Primary\_xxx' or 'Secondary\_xxx' folder alongside the session.

<div><figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 113707.png" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 113955.png" alt="" width="361"><figcaption></figcaption></figure></div>

3. Select the rgb folder as the directory.

<div><figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114102.png" alt="" width="360"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114205.png" alt="" width="359"><figcaption></figcaption></figure></div>

4. Click through the next few pages until you reach the templates page.
   1. The defaults on these pages are correct.

<div><figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114311.png" alt="" width="359"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114351.png" alt="" width="359"><figcaption></figcaption></figure></div>

5. Use either the '<mark style="color:$primary;">3D Maps</mark>' or the '<mark style="color:$primary;">PixelScout V4</mark>' template if its there.
   1. If there's no PixelScout template, one may be saved for later use.

<div><figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114449.png" alt="" width="359"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2026-06-04 101629.png" alt="" width="325"><figcaption></figcaption></figure></div>

6. If using the 3D Maps template, deselect steps 2 and 3 at the bottom.
7. If a PixelScout template is not available, one may be created using the steps below.

<details>

<summary>Creating a PixelScout Template</summary>

1. After de-selecting the 2nd and 3rd steps, click on '<mark style="color:blue;">Processing Options</mark>' in the bottom left corner.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114817.png" alt=""><figcaption></figcaption></figure>

2. Click on '<mark style="color:blue;">Save Template</mark>' in the bottom left corner of the new window.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114854.png" alt="" width="500"><figcaption></figcaption></figure>

3. Click '<mark style="color:blue;">Create New Template with Current Options...</mark>'

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114938.png" alt="" width="503"><figcaption></figcaption></figure>

4. Name it '<mark style="color:blue;">PixelScout</mark>' and Click '<mark style="color:blue;">OK</mark>'

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 115020.png" alt=""><figcaption></figcaption></figure>

5. Click 'OK' to return to the main Pix4D screen.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 115045.png" alt="" width="503"><figcaption></figcaption></figure>

</details>

8. Click '<mark style="color:blue;">Start</mark>' to process the data.

<figure><img src="../../../.gitbook/assets/Screenshot 2026-06-01 114543 (1).png" alt=""><figcaption></figcaption></figure>

9. When its done, look at the quality report. There are many things to look at. Use the expandables below for a little more detail on each. for 4 green checks (last one shouldn't be green). and errors and stuff.

<details>

<summary>Quality Check: 4 green checkmarks</summary>

The first 4 rows should have a green check, the 5th is yellow.

<figure><img src="../../../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Preview: No strange elevation changes.</summary>

This should be a good representation of the elevation changes of the calibration area.

<figure><img src="../../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Calibration Details: Initial Image Positions: No wandering</summary>

Ensure the path and photo locations represent the actual flight path taken by the drone

<figure><img src="../../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Calibration Details: Computed Image/GCPs/Manual Tie Points Positions: No large ellipses</summary>

Ensure the dots again follow the correct path and there are no large uncertainty ellipses around the photos. Some ellipses may be acceptable for unnatural circumstances. Also ensure there are little to no red dots

<mark style="color:green;">GOOD</mark> Example

<figure><img src="../../../.gitbook/assets/image (217).png" alt="" width="375"><figcaption></figcaption></figure>

<mark style="color:red;">BAD</mark> Examples

<figure><img src="../../../.gitbook/assets/image (218).png" alt="" width="375"><figcaption></figcaption></figure>



</details>

<details>

<summary>2D Keypoint Matches: Lots of black</summary>

Ensure there is plenty of black between all the dots. The picture below is ideal.

<figure><img src="../../../.gitbook/assets/image (220).png" alt="" width="563"><figcaption></figcaption></figure>

The picture below is acceptable as long as everything else looks good but it is not preferred. Much less connecting lines than this is not acceptable.

<figure><img src="../../../.gitbook/assets/image (221).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary>Absolute Geolocation Variance: No red numbers</summary>

Ensure there are no red numbers in this table. A couple red numbers may be acceptable if everything else looks good. However, it is usually a sign of a bad calibration due to long yaw error convergence times.

<figure><img src="../../../.gitbook/assets/image (222).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

<details>

<summary>Geolocation Orientational Variance: Low numbers</summary>

Ensure the RMS values in this table are low (<2-3 degrees)

<figure><img src="../../../.gitbook/assets/image (223).png" alt=""><figcaption></figcaption></figure>

</details>

10. If everything in the report looks acceptable, pix4d can be closed and you can move on to the next step.



## Calibration

1. Open the calibration gui application (same one used for 6x pixel alignment)
2. Go to the second tab, labeled pix4d.
3. Select the session folder, pix4d folder, and hw\_config file.
4. Output should be the session folder plug '\_cal'.
5. Run the calibration maker.
6. Study the chart that pops up after calibration completes.
   1. Ensure no line goes past +/- 2.5 degrees
   2. Make sure the lines do not deviate far from the average (e.g. large slopes, starting far from the average, large discontinuities other than on the turns, etc.)
7. When its done, open the new hw\_config file in the cal folder and look for pix4d calibration at the bottom with new values loaded in rig\_relatives\_deg.



## Calibrated Quicktile

1. Open quicktile again.
2. Use the same session folder
3. For the output, label it as the session plus '\_cal\_out' at the end.
4. In the advanced text box, type the following
   1. \--alignment\_cal\_file "..."
   2. copy the path of the 'quicktile.cal' file in the '\_cal' folder and paste the path (with quotes) where the 3 dots are.
5. Run the Quicktile.
6. When its done, look to make sure it looks much better than the original Quicktile.



## Applying to Camera

{% hint style="info" %}
NOTE: This is a good checkpoint to stop and make sure everything looks good before applying the calibration. It is easier to restart now than after applying the hw\_config.
{% endhint %}

1. in the '\_cal' folder, copy the 'h&#x77;_\__&#x63;onfig' file.&#x20;
   1. Not the original one
2. Paste the file into the firmware folder on the camera's SD card.
3. Power cycle the camera to apply the changes.
4. open the hw\_config file from the 'info' folder on the camera's files and ensure the calibration applied correctly.
   1. it should say 'Calibration: pix4d'
   2. The 'rig\_relatives' should be non-zero





## Cleanup/Saving Artifacts

1. Create/navigate to the corresponding serial number folder (e.g.. "123") in taurus, 21282-00 PixelScout Phase 4.
2. Copy the files from the calibration into a folder labeled 'Calibration'.
   1. Files should be organized in the following manner:
      1. Calibration
         1. Primary\_XXX
            1. \[all calibration files for primary camera]
         2. Secondary\_XXX
            1. \[all calibration files for secondary camera]

<figure><img src="../../../.gitbook/assets/Calibration Flight Artifacts (3).png" alt=""><figcaption><p>Example calibration artifacts folder</p></figcaption></figure>

