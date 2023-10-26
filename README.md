# voron
Voron Trident configuration and upgrades



# instalace BTT U2C

```shell
lsusb 
# select OpenMoko...
sudo nano /etc/network/interfaces.d/can0
```

```shell
allow-hotplug can0
  iface can0 can static
  bitrate 1000000
  up ip link set can0 txqueuelen 1024
```


https://www.klipper3d.org/CANBUS.html

test canbus: (connect device and run from rpi)
~/klippy-env/bin/python ~/klipper/scripts/canbus_query.py can0