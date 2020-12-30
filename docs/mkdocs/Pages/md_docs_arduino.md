---
title: Arduino


---

# Arduino


[RF24](/Classes/classRF24/) is fully compatible with Arduino boards

See [Arduino Board Reference](http://www.arduino.cc/en/Reference/Board) and [SPI Reference](http://arduino.cc/en/Reference/SPI) for more information

[RF24](/Classes/classRF24/) makes use of the standard hardware [SPI](/Classes/classSPI/) pins (MISO, MOSI, SCK) and requires two additional pins, to control the chip-select and chip-enable functions.

These pins must be chosen and designated by the user, in `[RF24](/Classes/classRF24/) radio(ce_pin, cs_pin);` and can use any available pins.


# Alternate SPI Support

[RF24](/Classes/classRF24/) supports alternate [SPI](/Classes/classSPI/) methods, in case the standard hardware [SPI](/Classes/classSPI/) pins are otherwise unavailable.


## Software Driven SPI

Software driven [SPI](/Classes/classSPI/) is provided by the [DigitalIO](https://github.com/greiman/DigitalIO) library

Setup:



1. Install the digitalIO library
2. Open [RF24_config.h](/Files/RF24__config_8h/#file-rf24_config.h) in a text editor. Uncomment the line 

```cpp
#define SOFTSPI
```

_Filename: .cpp_

or add the build flag/option 

```cpp
-DSOFTSPI
```

_Filename: .shell_



1. In your sketch, add 

```cpp
#include DigitalIO.h
```

_Filename: .cpp_

 
!!! note

    Pins are listed as follows and can be modified by editing the RF24_config.h file.
 

```cpp
#define SOFT_SPI_MISO_PIN 16
#define SOFT_SPI_MOSI_PIN 15
#define SOFT_SPI_SCK_PIN 14
```

_Filename: .cpp_

Or add the build flag/option 

```cpp
-DSOFT_SPI_MISO_PIN=16 -DSOFT_SPI_MOSI_PIN=15 -DSOFT_SPI_SCK_PIN=14
```

_Filename: .shell_


## Alternate Hardware (UART) Driven  SPI

The Serial Port (UART) on Arduino can also function in [SPI](/Classes/classSPI/) mode, and can double-buffer data, while the default [SPI](/Classes/classSPI/) hardware cannot.

The SPI_UART library is available at [TMRh20's Sketches repo](https://github.com/TMRh20/Sketches/tree/master/SPI_UART)

Enabling:



1. Install the SPI_UART library
2. Edit [RF24_config.h](/Files/RF24__config_8h/#file-rf24_config.h) and uncomment `#define SPI_UART`
3. In your sketch, add `#include <SPI_UART.h>`
SPI_UART [SPI](/Classes/classSPI/) Pin Connections


| NRF   | Arduino Uno Pin    |
|  -------- | -------- |
| MOSI   | TX(0)    |
| MISO   | RX(1)    |
| SCK   | XCK(4)    |
| CE   | User Specified    |
| CSN   | User Specified    |


SPI_UART on Mega boards requires soldering to an unused pin on the chip. See `#24 <[https://github.com/TMRh20/RF24/issues/24](https://github.com/TMRh20/RF24/issues/24)>`_ for more information on SPI_UART. 

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
