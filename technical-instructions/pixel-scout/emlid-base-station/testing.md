# Testing

## Information

This testing regiment is to ensure the base station functions correctly. It does not need to be tested with the PixelScout Payload.&#x20;

This can be revised to include testing with the payload to verify corrections output from the base station.&#x20;

## Required Equipment&#x20;

* [ ] Emlid RS3 Base Station w/ PixelScout Configuration Settings
* [ ] iPad or Cell Phone w/ mobile data.&#x20;
* [ ] Emlid Flow Application&#x20;
* [ ] Tripod that can support the Emlid Base Station&#x20;

## NTRIP Setup (one time)

{% hint style="info" %}
NTRIP Credentials need to be added to the Emlid Flow app on your iPad/Cell phone if it does not already have them. i.e. first time setup.&#x20;
{% endhint %}

Power the base station on.&#x20;

Connect to the base station using the Emlid Flow app. Connect using the bluetooth option.&#x20;

Select the Correction input page from the left hand menu.&#x20;

Select NTRIP over Bluetooth. Then enter your NTRIP credentials.

{% hint style="info" %}
The NTRIP credentials will remain persistant on your iPad/Cell phone. I am not certain if they are persistant to the base station. This needs to be evalutated as the base station should not ship out of the system with Sentera credentials loaded into them.&#x20;
{% endhint %}

## Instructions

{% stepper %}
{% step %}
### Go Outside

This test requires obtaining an RTK Fixed solution. This is highly unlikely to be achieved indoors.&#x20;
{% endstep %}

{% step %}
### Assemble Base Station&#x20;

Attached the base station to the tripod.&#x20;

Setup the tripod.&#x20;

Place the system away from buildings, roofs, etc. The base station requires a clear view of the sky.&#x20;
{% endstep %}

{% step %}
### Power the Base Station On

Power the base station on.

Connect to the base station via the Emlid Flow App using the Bluetooth option.&#x20;
{% endstep %}

{% step %}
### Start Corrections

Navigate to the the Corrections Input page fromt he left hand menu.&#x20;

Verify the corrections input is set to NTRIP over Bluetooth.&#x20;

Verify corrections are being recieved.&#x20;
{% endstep %}

{% step %}
### Verify Survey Status

Navigate to the Base Settings page from the left hand menu.&#x20;

Verify the base station has achieved and&#x20;


{% endstep %}
{% endstepper %}
