# Verification Processing (Needs Screenshots)

## Verification Processing

1. Create a new 'Verification' Folder.
2. Download the **session** and **info** folder from the verification flight into a 'Primary' or 'Secondary' folder in the 'Verification' folder for each camera.
3. Open 2 instances of the quicktile program. (one for each camera)
4. Select the verification flight session folders
5. Use '\_val\_out' for the output folder
6. Run the Quicktile Program.
7. Once completed, drag the .tif into QGIS and make sure it looks good.
   1. Straight lines (parking lines, edges of grass, etc) should be continuous with no breaks/jumps larger than a pixel or two.
   2. No stationary objects should look out of place.
8. Close QGIS and click 'discard' if prompted to save.



## Cleanup

1. create/navigate to a corresponding serial number folder in taurus, 21282-00 PixelScout Phase 4.
2. Copy the files from the verification into a folder labeled 'Verification'.
   1. Files should be organized in the following manner:
      1. Verification
         1. Primary
            1. \[all verification files for primary camera]
         2. Secondary
            1. \[all verification files for secondary camera]

<figure><img src="../../../.gitbook/assets/Verification Flight Artifacts (1).png" alt=""><figcaption><p>Example verification artifacts folder</p></figcaption></figure>
