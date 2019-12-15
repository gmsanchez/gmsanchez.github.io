---
layout: post
title:  "Headless Raspberry Pi Setup"
date:   2019-12-14 23:46:00 -0300
categories: Raspbian [Raspberry Pi]
---

This is useful if you are planning on install Raspbian and you can't find an USB keyboard in your house.

# Add “SSH” File to the SD Card Root
Enable SSH by placing a file named “ssh” (without any extension) onto the boot partition of the SD card

# Add your Wi-Fi network before booting
Edit `/etc/wpa_supplicant/wpa_supplicant.conf` and add the following

``network={
        ssid="YOUR SSID"
        psk="PASSWORD IN CLEARTEXT"
}``

If you don't want to save your Wi-Fi password in clear text, once the Raspberry Pi booted, you can run
``sudo su
wpa_passphrase "SSID" "PASSWORD" >> /etc/wpa_supplicant/wpa_supplicant.conf``

and then edit `/etc/wpa_supplicant/wpa_supplicant.conf` once again to remove the clear text password for the desired SSID.


## References
* [Headless Raspberry Pi Setup](https://hackernoon.com/raspberry-pi-headless-install-462ccabd75d0)
* [Configure WiFi connection in Raspbian Stretch Lite on Raspberry Pi](http://coffeetime.solutions/configure-wifi-connection-raspbian-stretch-lite-raspberry-pi/)
