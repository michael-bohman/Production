---
description: 'Owner: Simon'
---

# 🚧 65R Bad Pixel Replacemnt

Take BPR pictures.

1. Mount the gimbal to a drone and turn it on. Connect to the gimbal using usb.
2. Start a session for the each camera using the webpage.
   1. name it anything, the pictures won't be stored in the session.
3. Run the bpr pictures program and follow the instructions.
   1. The program must be edited in notepad to set the ip address for the camera being worked on.
4. Save the pictures created to a '\[PixelScout SN] BPR' folder.
5. Send the folder to zach/brian/jon for processing (WILL PROBABLY CHANGE)
6. After receiving the bprmap.csv file from processing, apply it to the cameras by placing it in the correct 'firmware' folder.
7. Power cycle the cameras and ensure it is saved to the 'info' folder.



Use the BPR capture tool first.<br>

* Edit the BPR Capture Tool in notepad and change the filepath to have your User ID, don't change anything else about the filepath.
* Edit the IP address at the top to use whatever you're using to connect to the camera (works with usb or Ethernet)
* Before any pictures are taken, start a session and call it whatever you want, the photos are stored on the SD card, not in the session folder.
* the password is '6636cedar'
* The "light table" is the board with the USB, tap the button to turn it on. make sure you hold it flat against the lens when you click enter after typing in the password.
* Try to check that the pictures are being saved to the SD Card folder before making much progress. It sucks to do everything to realize the pictures didn't save because the session wasn't started or something.

Save the 6 images to a folder on your machine.\
Open the 'bad\_pixel\_map\_v1.0.0' program and set the input folder to that folder. if you leave the output blank, itll save a new folder next to your input folder with a new name.\
Copy the 'bpr\_map.csv' file to the firmware folder of the camera, power-cycle, and open the image adjustment page on the website and check 'bad pixel replacement'. Refresh the page to make sure it saved.\
\
If you want to double check that it worked. Start a new session and take a picture. Use a metadata tool like 'ExifToolGUI' (david has some tool like this) and look a the XMP tags to make sure 'BPREnabled' equals 1
