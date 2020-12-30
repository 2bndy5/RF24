---
title: MRAA


---

# MRAA


MRAA is a Low Level Skeleton Library for Communication on GNU/Linux platforms See [MRAA docs](http://iotdk.intel.com/docs/master/mraa/index.html) for more information

[RF24](/Classes/classRF24/) supports all MRAA supported platforms, but might not be tested on each individual platform due to the wide range of hardware support:

[Report an RF24 bug or issue](https://github.com/2bndy5/RF24/issues)


# Setup Setup and installation

Build using the [MRAA library](http://iotdk.intel.com/docs/master/mraa/index.html) MRAA is not included.

1. Install, and build MRAA ```shell git clone [https://github.com/intel-iot-devkit/mraa.git](https://github.com/intel-iot-devkit/mraa.git) cd mraa mkdir build cd build cmake .. -DBUILDSWIGNODE=OFF sudo make install ```
2. Complete the install
open a text editor ```shell nano /etc/ld.so.conf ``` Add the line ``` /usr/local/lib/arm-linux-gnueabihf ```
Run ```shell sudo ldconfig ```
3. Install [RF24](/Classes/classRF24/), using MRAA See [Linux Installation](/Pages/md_docs_linux_install/#page-md_docs_linux_install)

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
