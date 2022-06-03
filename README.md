# I hacked MiBand 3, and here is how I did it

Detailed Writeup on how to use this Library

[I hacked MiBand 3, and here is how I did it. Part I](https://medium.com/@yogeshojha/i-hacked-xiaomi-miband-3-and-here-is-how-i-did-it-43d68c272391)

[I hacked MiBand 3, and here is how I did it Part II — Reverse Engineering to upload Firmware and Resources Over the Air](https://medium.com/@yogeshojha/i-hacked-miband-3-and-here-is-how-i-did-it-part-ii-reverse-engineering-to-upload-firmware-and-b28a05dfc308)

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
