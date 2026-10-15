---
description: 'Owner: Isaac'
---

# Gyro BIT Check

## Requirements

You will need <mark style="color:blue;">sbgCenter</mark> installed: \[insert link to installation instructions]

## Guide

* Open <mark style="color:blue;">sbgCenter</mark>
* Go to <mark style="color:blue;">`File > Import log`</mark>

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 120435.png" alt="" width="294"><figcaption></figcaption></figure>

* Click <mark style="color:blue;">`Ok`</mark>

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 120449.png" alt="" width="428"><figcaption></figcaption></figure>

* Import sbg-support log
  * Select input directory <mark style="color:blue;">`[PixSc S/N]>[Cal or Val]>[sensor]>info>logs>detail>####`</mark>
  * Ensure <mark style="color:blue;">`sbg-support`</mark> is selected and all others are deselected
  * Click <mark style="color:blue;">`Import Selected logs`</mark>&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 120512.png" alt="" width="510"><figcaption></figcaption></figure>

* Click the <mark style="color:blue;">`Add new graph`</mark> button

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 120740.png" alt="" width="425"><figcaption></figcaption></figure>

* Select <mark style="color:blue;">`Attitude>Euler Angles (°)`</mark> and click <mark style="color:blue;">`Add Graph`</mark>

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 115430.png" alt="" width="563"><figcaption></figcaption></figure>

* Select <mark style="color:blue;">`Status>IMU Status`</mark> and click <mark style="color:blue;">`Add Graph`</mark>

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 120033.png" alt="" width="563"><figcaption></figcaption></figure>

* You may close the <mark style="color:blue;">`Open new graph`</mark> window
* Scroll the bottom (blue-ish) bar to zoom in & out and to pan the view

<figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 143335.png" alt=""><figcaption></figcaption></figure>

* Check for any anomalies along the IMU Status lines

<div><figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 142821.png" alt=""><figcaption><p>GOOD: All "IMU Status" lines flat—no flags</p></figcaption></figure> <figure><img src="../../.gitbook/assets/Screenshot 2026-10-15 142611.png" alt=""><figcaption><p>BAD: Orange flags reading "0"</p></figcaption></figure></div>

* If good, continue with assembly/programming. If bad, reach out to engineering
