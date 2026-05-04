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
3. Use the pix4d login provided and an empty license

{% hint style="info" %}
NOTE: only use a new license if you plan on using the pix4d program often. There are limited licenses. Use another employees computer login if possible.
{% endhint %}







## Pix4d

1. Open pix4d twice from the desktop, one for primary and one for secondary.
2. Create a new project named the same as the session with '\_pix4d' at the end
   1. For the secondary camera, also add '\_2nd' at the end.
3. Select the rgb folder as the directory.
4. Click through the next few pages until you reach the templates page.
   1. All default settings are used for processing.
5. Use either the '3d maps' or the pixelscout template if its there.
   1. For the 3d maps, de-select everything but the first step.
   2. After deselecting the other steps, the template may be saved for later use.
6. Process the data.
7. When its done, look at the quality report. There are many things to look at. Use the expandables below for a little more detail on each. for 4 green checks (last one shouldn't be green). and errors and stuff.

<details>

<summary>Overall: 4 green checkmarks</summary>

The first 4 rows should have a green check, the 5th is yellow.

</details>

<details>

<summary>Next thing</summary>



</details>

<details>

<summary>Next thing</summary>



</details>





## Starting Quicktile

1. Open the quicktile program
2. Select each session folder (primary and secondary) as an input.
3. The output should be named the session plus '\_out' at the end.
4. Run the quicktiler.
5. When its done running. go to the out folder and find the .tif (photo icon).
6. Open QGIS and drag the .tif into it to see the pre-calibration stitched view. (NOT REQUIRED)





## Calibration

1. Open the calibration gui application (same one used for 6x pixel alignment)
2. Go to the second tab, labeled pix4d.
3. Select the session folder, pix4d folder, and hw\_config file.
4. Output should be the session folder plug '\_cal'.
5. Run the calibration maker.
6. When its done, open the new hw\_config file in the cal folder and look for pix4d calibration at the bottom with new values loaded in rig\_relatives\_deg.

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

1. asdf







## Cleanup/Saving Artifacts

1. Create/navigate to the corresponding serial number folder (e.g.. "123") in taurus, 21282-00 PixelScout Phase 4.
2. Copy the files from the calibration into a folder labeled 'Calibration'.
   1. Files should be organized in the following manner:
      1. Calibration
         1. Primary
            1. \[all calibration files for primary camera]
         2. Secondary
            1. \[all calibration files for secondary camera]

<figure><img src="../../../.gitbook/assets/Calibration Flight Artifacts (3).png" alt=""><figcaption><p>Example calibration artifacts folder</p></figcaption></figure>

