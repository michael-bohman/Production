# Gimbal Fault Isolation Manual



<details>

<summary>No Gimbal Communication </summary>

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Example:&#x20;

* Coms board programmed with no issues. Once gimbal is connected to camera and plugged into drone the camera lights flash red. The logs so this error above, indicating it is a coms board issue.&#x20;
{% endhint %}

Action&#x20;

1. Take camera off gimbal and take apart stack until you get to the coms board.&#x20;
2. Plug coms board into power at the coms board station.&#x20;
3. Identify if the coms board is getting power&#x20;
4. Try to re-program Coms board&#x20;

Solution

1. If no power on coms board message [Alex Stephens ](https://sentera.slack.com/archives/D09JHS0R6A3) and leave on his desk with note
2. If you are receiving power but can't reprogram it, message [Help-Embedded](https://sentera.slack.com/archives/C0117U18P6U) to diagnoise the issue&#x20;
3. If coms board is no longer useable, update build on [SOS](https://live.sosinventory.com/BuildAssembly) and grab another from inventory

</details>

<details>

<summary>When testing gimbal the camera twitches after initialization </summary>

This is a different issue then switching the black cords. This issue would happen after the camera initializes and its a slow twitch.&#x20;



1. Switch out the gimbal (possible wiring harness issue)
   1. Use the same stack&#x20;
2. Connect camera to basecam&#x20;
   1. Reload the backup manager 6X or 65R gimbal file&#x20;

</details>

<details>

<summary>No motor control on the gimbal</summary>

This is likely a motor controller issue. The coms board should appear in the previous logs. If you don't see any sign of the logs showing gimbal operation, it could be a coms issue. See no gimbal connection issue for more info&#x20;

{% embed url="https://app.gitbook.com/o/r7P0NuYTKsmybK4bmqti/s/ycfHWm9ckUsdZmfqLCYz/~/edit/~/changes/207/fault-isolation/gimbal-fault-isolation-manual#no-gimbal-communication" %}

<figure><img src="../.gitbook/assets/image (173).png" alt=""><figcaption></figcaption></figure>

1. Take apart the stack and remove the motor controller&#x20;
2. Pull in motor controller to a 12v power adapter and confirm it's getting power&#x20;
   1. If no power, message Alex Stephens describing issue. Replace the motor controller for your stack&#x20;
   2. If you have power, check step 3&#x20;
3. Plug in coms board as well to the 24v power adapter to confirm it's getting power
4. If all signs are normal for COMS and Motor Controller. Check the wiring harness. Grab another gimbal and switch it out to see if that solves the issue. If so, you know that the faulty gimbal needs a new wiring harness&#x20;

</details>

<details>

<summary>Slow IMU Issue </summary>

The camera slowly drifts when starting up. This issue is caused by the gyro getting too much vibration, which we have learned is caused by the fan

1. Switch out the fan until the drift stops
2. Contact Wayne if you want to confirm with the computer

</details>

<details>

<summary>Slow twitch every few seconds </summary>

1. Connect camera to basecam&#x20;
   1. Reload the backup manager 6X or 65R gimbal file&#x20;

</details>

<details>

<summary>Camera keep power cycling while on gimbal</summary>

This issue can show up in multiple ways. It is likely the issue when the camera is functioning as normal on the gimbal and then restarts after losing power.&#x20;

1. Rule out motor controller issue by plugging it in and seeing if that board is functioning as normal. If no, continue step 2.&#x20;
2. Grab another gimbal and switch it out to see if that solves the issue. If so, you know that the faulty gimbal needs a new wiring harness&#x20;

</details>
