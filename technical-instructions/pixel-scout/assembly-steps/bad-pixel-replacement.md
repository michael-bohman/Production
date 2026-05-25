---
description: 'Owner: Simon'
---

# 📷 Bad Pixel Replacement

## Equipment Needed&#x20;

| 65R Camera         | Power cable              | USB Cable |
| ------------------ | ------------------------ | --------- |
| Light Table or Cap | Softwares (listed below) |           |
|                    |                          |           |

## Notes&#x20;



## Prep

1. If not already done, download the BPR programs here:
   1. [#bpr-files](../../../space-and-general/software-installation-guide.md#bpr-files "mention")
2. If a metadata file viewer is not already installed, download one.
   1. [#exif-tool-gui](../../../space-and-general/software-installation-guide.md#exif-tool-gui "mention")





## Guide

### Taking Pictures

1. Plug in a 65R with power and USB.
2. Start a session manually using the webpage (192.168.42.1).
   1. name it anything, the pictures won't be stored in the session
      1. 'bprcreation' is usually used for clarification on an empty session folder.
3. Right click the BPR Pictures program and select 'Edit in Notepad'.
   1. Change the IP Address to 192.168.42.1 if not already set.
   2. Save and close notepad.
4. Run the bpr pictures program and follow the instructions.
5. Save the pictures created to a '\[PixelScout SN] BPR' folder on your local machine.

### Processing

1. Open the 'bad\_pixel\_map\_gui.exe' application.
2. For the input folder, navigate to and open the folder containing the 6 pictures taken earlier.
3. Either choose an output folder or leave it blank for a new folder right next to the input folder titled '\[input folder name]\_bad\_pixels'



### Application

1. Once you have the files from the program, copy the 'bpr\_map.csv' file to the 'firmware' folder on the camera's SD card.
2. Power cycle the camera to apply the changes.
3. Connect a usb cable to the powered-on camera and navigate to '192.168.42.1' in a browser.
4. Go to the <mark style="color:$primary;">Image Adjustment</mark> tab and check '<mark style="color:$primary;">Bad Pixel Replacement</mark>' and click '<mark style="color:$primary;">Apply</mark>'.



### Check

1. Power on the camera and connect to it via usb.
2. Start a new session and name it anything.
3. Take a photo.
   1. This photo does not need to be of anything specific.
4. Open a metadata viewer and navigate to the photo you just took.
5. Look for the 'BPREnabled' XMP tag and ensure it is set to '1'.
