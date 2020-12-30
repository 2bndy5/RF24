---
title: General Linux/Raspberry Pi


---

# General Linux/Raspberry Pi


[RF24](/Classes/classRF24/) supports a variety of Linux based devices via various drivers. Some boards like RPi can utilize multiple methods to drive the [GPIO](/Classes/classGPIO/) and [SPI](/Classes/classSPI/) functionality.


# Potential PreConfiguration

If [SPI](/Classes/classSPI/) is not already enabled, load it on boot:



```cpp
sudo raspi-config
```

_Filename: .shell_



1. Update the tool via the menu as required
2. Select **Advanced** and **enable the [SPI](/Classes/classSPI/) kernel module**
3. Update other software and libraries 

```cpp
sudo apt-get update
sudo apt-get upgrade
```

_Filename: .shell_


# Build Options

The default build on Raspberry Pi utilizes the included [BCM2835 driver](http://www.airspayce.com/mikem/bcm2835)

See output from `./configure --help` for available build options

Configure the build options automatically by running 

```cpp
./configure
```

_Filename: .shell_


## Manual install



```cpp
make
sudo make install
```

_Filename: .shell_


# Pins Connections and Pin Configuration

Using pin 15/GPIO 22 for CE, pin 24/GPIO8 (CE0) for CSN

Can use any available [SPI](/Classes/classSPI/) BUS for CSN.

In general, use `[RF24](/Classes/classRF24/) radio(<ce_pin>, <a>*10+<b>);` for proper constructor to address correct spi device at /dev/spidev<a>.<b>

Choose any [GPIO](/Classes/classGPIO/) output pin for radio CE pin.


## General Contructor

`[RF24](/Classes/classRF24/) radio(22, 0);`


## MRAA Constructor

`[RF24](/Classes/classRF24/) radio(15, 0);`

See [MRAA docs about the Raspberry Pi](http://iotdk.intel.com/docs/master/mraa/rasppi.html)


## SPI_DEV Constructor

`[RF24](/Classes/classRF24/) radio(22, 0);`

See [Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/usage/gpio/) about using the [GPIO](/Classes/classGPIO/) pins


| PIN   | NRF24L01   | RPI   | RPi -P1 Connector    |
|  -------- | -------- | -------- | -------- |
| 1   | GND   | rpi-gnd   | 25    |
| 2   | VCC   | rpi-3v3   | 17    |
| 3   | CE   | rpi-gpio22   | 15    |
| 4   | CSN   | rpi-gpio8   | 24    |
| 5   | SCK   | rpi-sckl   | 23    |
| 6   | MOSI   | rpi-mosi   | 19    |
| 7   | MISO   | rpi-miso   | 21    |
| 8   | IRQ   | -   | -    |


Based on the arduino lib from J. Coliz [maniacbug@ymail.com](mailto:maniacbug@ymail.com)

the library was berryfied by Purinda Gunasekara [purinda@gmail.com](mailto:purinda@gmail.com)

then forked from github stanleyseow/RF24 to [https://github.com/jscrane/RF24-rpi](https://github.com/jscrane/RF24-rpi)

Network lib also based on [https://github.com/farconada/RF24Network](https://github.com/farconada/RF24Network)

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
