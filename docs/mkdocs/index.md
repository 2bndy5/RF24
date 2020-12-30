---
title: Introduction


---

# Introduction


[RF24](/Classes/classRF24/) Revamped is a simplified and extensible API for TMRh20's popular Optimized High Speed Driver for nRF24L01(+) 2.4GHz Wireless Transceiver 


# Goals Design Goals

This library fork is still designed to be...



* More compliant with the manufacturer specified operation of the chip, while allowing advanced users to work outside the recommended operation.
* Utilize the capabilities of the radio to their full potential via multiple platforms (i.e. Arduino & Raspberry Pi)
* More reliable, responsive, bug-free and feature rich
* Easy for beginners to use, with well documented examples and features
* Consumed with a public interface that's similar to other Arduino standard libraries

# Change Log

See [the releases](http://github.com/2bndy5/RF24/releases) for a details on what was changed in each version of the library


# Useful References



* [[RF24](/Classes/classRF24/) Class Documentation]([RF24](/Classes/classRF24/))
* Support & Configuration
* [Source Code](https://github.com/2bndy5/RF24/tree/revamp)
* [nRF24L01 v2.0 Datasheet](http://github.com/2bndy5/RF24/raw/master/datasheets/nRF24L01_datasheet_v2.pdf)
* [nRF24L01+ v1.0 Datasheet](http://github.com/2bndy5/RF24/raw/master/datasheets/nRF24L01P_datasheet_v1.pdf)

# Platform Support Pages



* [Arduino (Uno, Nano, Mega, Due, Galileo, etc)](/Pages/md_docs_arduino/#page-md_docs_arduino)
* [ATTiny](/Pages/md_docs_attiny/#page-md_docs_attiny)
* [Linux Installation](/Pages/md_docs_linux_install/#page-md_docs_linux_install)
    * [Linux/RPi General](/Pages/md_docs_rpi_general/#page-md_docs_rpi_general)
    * [MRAA (Galileo, Edison, etc) supported board](/Pages/md_docs_mraa/#page-md_docs_mraa)
    * LittleWire
* [Cross-compilation for linux devices](/Pages/md_docs_cross_compilation/#page-md_docs_cross_compilation)

# General Microcontroller Pin layout

See the individual board support pages (links in the sidebar) for more info

[![https://lastminuteengineers.com/wp-content/uploads/2018/07/Pinout-nRF24L01-Wireless-Transceiver-Module.png](/images/https://lastminuteengineers.com/wp-content/uploads/2018/07/Pinout-nRF24L01-Wireless-Transceiver-Module.png)](https://lastminuteengineers.com/nrf24l01-arduino-wireless-communication/#nrf24l01-transceiver-module-pinout)

The table below shows how to connect the the pins of the NRF24L01(+) to different boards. Only the IRQ, CE, and CSN pins are configurable.


| NRF24L01   | Arduino UNO   | ATtiny25/45/85<sup>1</sup> | ATtiny44/84<sup>2</sup> | LittleWire<sup>3</sup> | RPi   | RPi -P1 Connector    |
|  -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| GND   | GND   | pin 4   | pin 14   | GND   | rpi-gnd   | 25    |
| VCC   | 3.3V   | pin 8   | pin 1   | regulator 3.3V required   | rpi-3v3   | 17    |
| CE   | digIO 7   | pin 2   | pin 12   | pin to 3.3V   | rpi-gpio22   | 15    |
| CSN   | digIO 8   | pin 3   | pin 11   | RESET   | rpi-gpio8   | 24    |
| SCK   | digIO 13   | pin 7   | pin 9   | SCK   | rpi-sckl   | 23    |
| MOSI   | digIO 11   | pin 6   | pin 7   | MOSI   | rpi-mosi   | 19    |
| MISO   | digIO 12   | pin 5   | pin 8   | MISO   | rpi-miso   | 21    |
| IRQ   | -   | -   | -   | -   | -   | -    |


<sup>1</sup>[https://learn.sparkfun.com/tutorials/tiny-avr-programmer-hookup-guide/attiny85-use-hints](https://learn.sparkfun.com/tutorials/tiny-avr-programmer-hookup-guide/attiny85-use-hints)
<sup>2</sup>[http://highlowtech.org/?p=1695](http://highlowtech.org/?p=1695)
<sup>3</sup>[http://littlewire.cc](http://littlewire.cc)

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
