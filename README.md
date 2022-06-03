# I hacked MiBand 3, and here is how I did it

![1_sC2gb3SimjuTXXQO4wVxGA](https://miro.medium.com/max/700/1*4M9tV1tfWS0Q6tSzaeYfxg.jpeg)

![1_sC2gb3SimjuTXXQO4wVxGA](https://user-images.githubusercontent.com/17223002/171925123-7ef0e595-f150-48c4-b844-4e04d404ed58.png)

Detailed Writeup on how to use this Library

[I hacked MiBand 3, and here is how I did it. Part I](https://medium.com/@yogeshojha/i-hacked-xiaomi-miband-3-and-here-is-how-i-did-it-43d68c272391)

[I hacked MiBand 3, and here is how I did it Part II — Reverse Engineering to upload Firmware and Resources Over the Air](https://medium.com/@yogeshojha/i-hacked-miband-3-and-here-is-how-i-did-it-part-ii-reverse-engineering-to-upload-firmware-and-b28a05dfc308)

# Video POCs


## MI Band Pairing and Sending Calls

[![POC](https://img.youtube.com/vi/W-18ATOgwmA/0.jpg)](https://www.youtube.com/watch?v=W-18ATOgwmA)

## Uploading Firmware OTA

[![POC](https://img.youtube.com/vi/mubNS-8hh0I/0.jpg)](https://www.youtube.com/watch?v=mubNS-8hh0I)

# Run

### Install dependencies

`pip install -r requirements.txt`

### Connection to MiBand

Turn on your Bluetooth

Unpair you MiBand2 from current mobile apps

Find out your MiBand3 MAC address

```sudo hcitool lescan```

Run this to auth device

```python main.py MAC_ADDRESS --init```

If you having problems(BLE can glitch sometimes)

```sudo hciconfig hci0 reset```

### If you have trouble installing bluepy

```sudo apt-get install libglib2-dev  ```


### Fix hcitool I/O Error

```sudo service bluetooth restart  ```
