# sensorgnome-pi
sensorgnome software running on a raspberry Pi 2 or 3

Disk image releases and updates are available from

  http://public.sensorgnome.org/RaspberryPi2_Sensorgnome_Images

This repository tracks changes to config and other source files,
using the 2017-02-24 release as the starting point.

Because git does not preserve file ownership, you should obtain
these files via the updates or images available above.

**DO NOT** install files directly from this repo unless you know what
you're doing - otherwise, you might disable your SG.  The file
*ls-AlR.txt* in this repo lists files with their correct ownership and
file permissions, for those who choose to swim beyond the buoy line.

Please use this repository to report issues with the sensorgnome software
on the Raspberry Pi.

### Power consumption ###
- includes DC/DC converter + RPi 3 + **No GPS** +  ethernet cable to laptop

This table shows power consumption per RTLSDR is ~ 0.65W higher than
for a funcubedongle Pro Plus.

Pi State | rtlsdr state | current draw (A) @ 12.50V  | Power (W)
---|---|---|---
idle| unplugged |  0.15 | 1.9
idle|  plugged in | 0.20 | 2.5
idle| rtl_tcp awaiting connections | 0.29 | 3.6
idle | rtl_tcp streaming i/Q -> /dev/null | 0.29 | 3.6
idle | rtl_tcp killed with SIGKILL | 0.29 | 3.6
idle | rtl_tcp killed with SIGTERM | 0.19 | 2.4
pulse detection | **1 rtlsdr** sampling @ 240000 Hz (one 7s tag active) | 0.29 | 3.6
pulse detection | **2 rtlsdr** sampling @ 240000 Hz (one 7s tag active) | 0.43 | 5.4
pulse detection | **3 rtlsdr** sampling @ 240000 Hz (one 7s tag active) | 0.57 | 7.1
pulse detection | **1 funcubeProPlus** sampling @ 48000 Hz (one 7s tag active) | 0.24 |3
pulse detection | **2 funcubeProPlus** sampling @ 48000 Hz (one 7s tag active) | 0.32 | 4
pulse detection | **3 funcubeProPlus** sampling @ 48000 Hz (one 7s tag active) | 0.41 | 5.1
