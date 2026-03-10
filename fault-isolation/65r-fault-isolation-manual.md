# 65R Fault Isolation Manual

## Common Issues

<details>

<summary>Poor Communication/Random dropouts</summary>

Poor camera communication can result in slower transfer speeds, random dropouts, and USB connectivity errors. Here are a few steps to take to diagnose it

1. Open a command prompt and type the following:

```
ping 192.168.42.1
```

{% hint style="info" %}
You can add ' -t' to the end of it to run it continuously so you can monitor the connection while working with the camera. To stop, hit ctrl+c.
{% endhint %}

2. Watch for the response times. They should be <=1ms. If they are consistently higher than 1 ms, the computer is trying to connect with another device on the John Deere network that uses the same IP Address as the cameras. A good fix is to connect to Sentera Guest WIFI.
3. If you are getting errors, hit windows+r, type 'ncpa.cpl' and click 'OK'.
4. If there are only 2 things on this page, it is likely that the computer is not seeing the device.

</details>
