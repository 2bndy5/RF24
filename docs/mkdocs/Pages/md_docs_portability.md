---
title: RF24 Portability


---

# RF24 Portability


The [RF24](/Classes/classRF24/) radio driver mainly utilizes the [Arduino API](http://arduino.cc/en/reference/homePage) for [GPIO](/Classes/classGPIO/), [SPI](/Classes/classSPI/), and timing functions, which are easily replicated on various platforms.

Support files for these platforms are stored under _RF24/utility_, and can be modified to provide the required functionality. 


# Basic Hardware Template


## RF24/utility

The [RF24](/Classes/classRF24/) library now includes a basic hardware template to assist in porting to various platforms.

The following files can be included to replicate standard Arduino functions as needed, allowing devices from ATTiny to Raspberry Pi to utilize the same core [RF24](/Classes/classRF24/) driver.


| File   | Purpose    |
|  -------- | -------- |
| [RF24_arch_config.h](/Files/RF24__arch__config_8h/#file-rf24_arch_config.h) | Basic Arduino/AVR compatibility, includes for remaining support files, etc    |
| [includes.h](/Files/includes_8h/#file-includes.h) | Linux only. Defines specific platform, include correct _RF24_arch_config_ file    |
| [spi.h](/Files/spi_8h/#file-spi.h) | Provides standardized [SPI](/Classes/classSPI/) (transfer()) methods    |
| [gpio.h](/Files/gpio_8h/#file-gpio.h) | Provides standardized [GPIO](/Classes/classGPIO/) ([digitalWrite()](/Files/RF24__arch__config_8h/#define-digitalwrite)) methods    |
| [compatibility.h](/Files/compatibility_8h/#file-compatibility.h) | Provides standardized timing ([millis()](/Files/RF24__arch__config_8h/#define-millis) and [delay()](/Files/RF24__arch__config_8h/#define-delay)) methods    |
| your_custom_file.h   | Provides access to custom drivers for spi, gpio, etc    |


Examples are provided via the included hardware support templates in _RF24/utility_

See the modules.html page for examples of class declarations 


## Device Detection



1. The main detection for Linux devices is done in the configure script, with the _[includes.h](/Files/includes_8h/#file-includes.h)_ from the proper hardware directory copied to _RF24/utility/includes.h_
2. Secondary detection is completed in _[RF24_config.h](/Files/RF24__config_8h/#file-rf24_config.h)_, causing the _include.h_ file to be included for all supported Linux devices.
3. _RF24.h_ contains the declaration for [SPI](/Classes/classSPI/) and [GPIO](/Classes/classGPIO/) objects 'spi' and 'gpio' to be used for porting-in related functions. 

# Ported Code

To have your ported code included in this library, or for assistance in porting, create a pull request or open an issue at [https://github.com/TMRh20/RF24](https://github.com/TMRh20/RF24)

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
