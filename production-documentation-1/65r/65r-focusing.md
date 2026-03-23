---
description: Stage 3 in the 65R Process 21030-02
---

# 65R Focusing

## Notes

For focusing 21030-04 cameras for PixelScout systems, refer to the PixelScout assembly steps. There are a few key differences in the process. [1-pixelscout-65r-focusing.md](../../technical-instructions/pixel-scout/assembly-steps/1-pixelscout-65r-focusing.md "mention")

## Required Materials/Equipment

* Tripod
* 65R mount
* Power cable
* Focusing USB-C cable

## Focusing

1.  Place the camera in the bracket and attach it to a tripod.

    <figure><img src="../../.gitbook/assets/image (28).png" alt="" width="302"><figcaption></figcaption></figure>
2. Plug in power/USB to the camera and the wall/computer.
3. Navigate to 19.168.42.1 in chrome.
4. In the 'Session Control' area of the webpage, click 'Start Session'.
   1.  Verify that he lights turn green on the camera and no errors are displayed in the webpage.

       <figure><img src="../../.gitbook/assets/image (29).png" alt="" width="351"><figcaption></figcaption></figure>
5. Position the camera such that the targets or subjects are in view.
   1. For -02 Cameras, point the camera out of the window.
6. In file explorer, navigate to //192.168.42.1 and go to data>snapshosts>web\_session.
7.  In the 'Trigger Control' area of the webpage, click 'Take Photo'.

    <figure><img src="../../.gitbook/assets/image (30).png" alt="" width="395"><figcaption></figcaption></figure>
8. Go to the new session and look at the photo you just took.
9. If it is not completely in focus, turn the lens to readjust focus.
   1. Clockwise (facing camera): Pushes focal distance outwards.
   2.  Counter-clockwise (facing camera): pulls focal distance closer.

       <figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>
10. Once you are close to being in focus, start tightening the locking ring after each adjustment.
    1. Tightening the locking ring will slightly alter the focal length. This mean that it must be tight to get an accurate depiction of the focus quality.
    2.  Ensure the locking ring screw is positioned over a screw that has already been installed and not an open screw hole. These open holes are used to install the lens shroud and cannot be covered up.

        <figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
11. Repeat steps 7-10 until the photo is in focus.
    1. Compare your photo to the reference photo decide if it is focused enough or not.
       1. look at fences (close and far), plants, powerlines, etc.
    2. Make sure to check many spots around the picture, including the edges, center, forground and background.
       1. Prioritize objects in the mirror at about 50-150 feet away.
12. Once the camera is focused, power cycle it by unplugging it and plugging it back in.
13. Create a new session named 'Focus'.

    <figure><img src="../../.gitbook/assets/image (33).png" alt="" width="287"><figcaption></figcaption></figure>
14. Take about 10-20 photos, turning the camera to a new angle slightly each time.
    1. Get a wide variety of angles with good overlap.
15. Put the lens cap over the lens and take a photo. Rename this one in the file explorer to 'Cap Photo'.
16. Focusing is complete.&#x20;
