---
description: How to process data and create/apply a calibration file.
---

# Calibration

Note: This is very rudamentary and will be refined later. This is just for a refresher after the weekend.



## Setup

1. copy session and info folder into a 'Primary' folder inside the serial number folder

## Pix4d

1. open pix4d twice from the desktop, one for primary and one for secondary.
2. Create a new project named the same as the session with '\_pix4d' at the end
   1. For the secondary camera, also add '\_2nd' at the end.
3. select the rgb folder as the directory.
4. use either the '3d maps' or the pixelscout template if its there.
   1. for the 3d maps, de-select everything but the first step.
5. process the data.
6. When its done, look at the quality report for 4 green checks (last one shouldn't be green). and errors and stuff.

## Starting Quicktile

1. open quicktile
2. select the session folder as an input
3. the output should be named the session plus '\_out' at the end.
4. run the quicktiler.
5. When its done running. go to the out folder and find the .tif (photo icon).
6. open QGIS and drag the .tif into it to see the pre-calibration stitched view.

## Calibration

1. open the calibration gui application (same one used for 6x pixel alignment)
2. go to the second tab, labeled pix4d.
3. select the session folder, pix4d folder, and hw\_config file.
4. output should be the session folder plug '\_cal'.
5. run the calibration maker.
6. when its done, open the new hw\_config file in the cal folder and look for pix4d calibration at the bottom with new values loaded in rig\_relatives\_deg.

## Calibrated Quicktile

1. open quicktile again.
2. use the same session folder
3. for the output, label it as the session plus '\_cal\_out' at the end.
4. in the advanced text box, type the following
   1. \--alignment\_cal\_file "..."
   2. copy the path of the 'quicktile.cal' file in the '\_cal' folder and paste the path (with quotes) where the 3 dots are.
5. Run the quicktile.
6. When its done, look to make sure it looks much better than the original quicktile.



Calibration is complete. Fly the Verification flight
