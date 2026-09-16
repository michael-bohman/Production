---
description: 'Owner: Isaac'
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
3. Right click the "bad\_pixel\_image\_capture.bat" program and select 'Edit in Notepad'.
   1. Change the IP Address to 192.168.42.1 if not already set.
   2. Change the "known\_hosts" path match your system
      1. likely "C:\Users\\\[username]\\.ssh\known\_hosts"
   3. Save and close notepad.
4. Run the bpr pictures program and follow the instructions.
   1. If prompted for a password, use "6636cedar"
5. Save the pictures created at "\\\192.168.42.1\sdcard" to a BPR folder on your local machine.

<figure><img src="../../../.gitbook/assets/image (208).png" alt="" width="339"><figcaption></figcaption></figure>

### Dibris Check

1. Open img\_bayer\_bright\_100.tif.
2. Check for dibris as seen in the image:
3. If any dibris is found:
   1. disassemble the camera.
   2. clean the sensor with compressed air.
   3. restart from the focusing step

<figure><img src="../../../.gitbook/assets/image (4) (3).png" alt="" width="375"><figcaption></figcaption></figure>

### Processing

1. Open the 'bad\_pixel\_map\_gui.exe' application.
2. For the input folder, navigate to and open the folder containing the 6 pictures taken earlier.
3. Either choose an output folder or leave it blank for a new folder right next to the input folder titled '\[input folder name]\_bad\_pixels'
4. Click 'Run'

<figure><img src="../../../.gitbook/assets/image (209).png" alt="" width="375"><figcaption></figcaption></figure>

5. Ensure the program completes successfully and the number of bad pixels is reasonable.
   1. Bad pixels should be in the range of 100-1000 roughly, with most 200-600.

<figure><img src="../../../.gitbook/assets/image (210).png" alt="" width="375"><figcaption></figcaption></figure>

6. Ensure a folder has been created and has everything in it.
   1. If output was left blank, it should be next to the input folder with name '\[input folder name]\_bad\_pixels'

<figure><img src="../../../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>







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

<figure><img src="../../../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>
