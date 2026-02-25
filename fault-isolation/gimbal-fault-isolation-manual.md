# Gimbal Fault Isolation Manual

<details>

<summary>No Gimbal Communication</summary>

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

