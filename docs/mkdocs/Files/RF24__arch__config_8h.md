---
title: utility/Template/RF24_arch_config.h


---

# utility/Template/RF24_arch_config.h


 [More...](#detailed-description)







## Types

|                | Name           |
| -------------- | -------------- |
| typedef uint16_t | **[prog_uint16_t](/Files/RF24__arch__config_8h/#typedef-prog_uint16_t)**  |





## Defines

|                | Name           |
| -------------- | -------------- |
|  | **[RF24_LINUX](/Files/RF24__arch__config_8h/#define-rf24_linux)**  |
|  | **[_BV](/Files/RF24__arch__config_8h/#define-_bv)**(x)  |
|  | **[_SPI](/Files/RF24__arch__config_8h/#define-_spi)**  |
|  | **[IF_SERIAL_DEBUG](/Files/RF24__arch__config_8h/#define-if_serial_debug)**(x)  |
|  | **[PSTR](/Files/RF24__arch__config_8h/#define-pstr)**(x)  |
|  | **[printf_P](/Files/RF24__arch__config_8h/#define-printf_p)**  |
|  | **[strlen_P](/Files/RF24__arch__config_8h/#define-strlen_p)**  |
|  | **[PROGMEM](/Files/RF24__arch__config_8h/#define-progmem)**  |
|  | **[pgm_read_word](/Files/RF24__arch__config_8h/#define-pgm_read_word)**(p)  |
|  | **[PRIPSTR](/Files/RF24__arch__config_8h/#define-pripstr)**  |
|  | **[pgm_read_byte](/Files/RF24__arch__config_8h/#define-pgm_read_byte)**(p)  |
|  | **[LOW](/Files/RF24__arch__config_8h/#define-low)**  |
|  | **[HIGH](/Files/RF24__arch__config_8h/#define-high)**  |
|  | **[INPUT](/Files/RF24__arch__config_8h/#define-input)**  |
|  | **[OUTPUT](/Files/RF24__arch__config_8h/#define-output)**  |
|  | **[digitalWrite](/Files/RF24__arch__config_8h/#define-digitalwrite)**(pin, value)  |
|  | **[pinMode](/Files/RF24__arch__config_8h/#define-pinmode)**(pin, direction)  |
|  | **[delay](/Files/RF24__arch__config_8h/#define-delay)**(milisec)  |
|  | **[delayMicroseconds](/Files/RF24__arch__config_8h/#define-delaymicroseconds)**(usec)  |
|  | **[millis](/Files/RF24__arch__config_8h/#define-millis)**()  |



## Detailed Description



























General defines and includes for RF24/Linux 



## Types Documentation

### typedef prog_uint16_t

```cpp
typedef uint16_t prog_uint16_t;
```
































## Macro Documentation

### define RF24_LINUX

```cpp
#define RF24_LINUX
```





























### define _BV

```cpp
#define _BV(
    x
) (1 << (x))
```





























### define _SPI

```cpp
#define _SPI spi
```





























### define IF_SERIAL_DEBUG

```cpp
#define IF_SERIAL_DEBUG(
    x
)
```





























### define PSTR

```cpp
#define PSTR(
    x
) (x)
```





























### define printf_P

```cpp
#define printf_P printf
```





























### define strlen_P

```cpp
#define strlen_P strlen
```





























### define PROGMEM

```cpp
#define PROGMEM
```





























### define pgm_read_word

```cpp
#define pgm_read_word(
    p
) (*(p))
```





























### define PRIPSTR

```cpp
#define PRIPSTR "%s"
```





























### define pgm_read_byte

```cpp
#define pgm_read_byte(
    p
) (*(p))
```





























### define LOW

```cpp
#define LOW [GPIO::OUTPUT_LOW](/Classes/classGPIO/#variable-output_low)
```





























### define HIGH

```cpp
#define HIGH [GPIO::OUTPUT_HIGH](/Classes/classGPIO/#variable-output_high)
```





























### define INPUT

```cpp
#define INPUT [GPIO::DIRECTION_IN](/Classes/classGPIO/#variable-direction_in)
```





























### define OUTPUT

```cpp
#define OUTPUT [GPIO::DIRECTION_OUT](/Classes/classGPIO/#variable-direction_out)
```





























### define digitalWrite

```cpp
#define digitalWrite(
    pin,
    value
) [GPIO::write](/Classes/classGPIO/#function-write)(pin, value)
```





























### define pinMode

```cpp
#define pinMode(
    pin,
    direction
) [GPIO::open](/Classes/classGPIO/#function-open)(pin, direction)
```





























### define delay

```cpp
#define delay(
    milisec
) [__msleep](/Files/compatibility_8h/#function-__msleep)(milisec)
```





























### define delayMicroseconds

```cpp
#define delayMicroseconds(
    usec
) [__usleep](/Files/compatibility_8h/#function-__usleep)(usec)
```





























### define millis

```cpp
#define millis(
    
) [__millis](/Files/compatibility_8h/#function-__millis)()
```































## Source code

```cpp
/*
 * Copyright (C) 2011 J. Coliz <maniacbug@ymail.com>
 *
 * This program is free software; you can redistribute it and/or
 * modify it under the terms of the GNU General Public License
 * version 2 as published by the Free Software Foundation.
 *
 */

#ifndef __ARCH_CONFIG_H__
#define __ARCH_CONFIG_H__

#define RF24_LINUX

#include <stddef.h>
#include "spi.h"
#include "gpio.h"
#include "compatibility.h"
#include <stdint.h>
#include <stdio.h>
#include <time.h>
#include <string.h>
#include <sys/time.h>

#define _BV(x) (1 << (x))
#define _SPI spi

#undef SERIAL_DEBUG
#ifdef SERIAL_DEBUG
    #define IF_SERIAL_DEBUG(x) ({x;})
#else
    #define IF_SERIAL_DEBUG(x)
#endif

// Avoid spurious warnings
#if 1
    #if !defined(NATIVE) && defined(ARDUINO)
        #undef PROGMEM
        #define PROGMEM __attribute__(( section(".progmem.data") ))
        #undef PSTR
        #define PSTR(s) (__extension__({static const char __c[] PROGMEM = (s); &__c[0];}))
    #endif
#endif

typedef uint16_t prog_uint16_t;
#define PSTR(x) (x)
#define printf_P printf
#define strlen_P strlen
#define PROGMEM
#define pgm_read_word(p) (*(p))
#define PRIPSTR "%s"
#define pgm_read_byte(p) (*(p))

// Function, constant map as a result of migrating from Arduino
#define LOW GPIO::OUTPUT_LOW
#define HIGH GPIO::OUTPUT_HIGH
#define INPUT GPIO::DIRECTION_IN
#define OUTPUT GPIO::DIRECTION_OUT
#define digitalWrite(pin, value) GPIO::write(pin, value)
#define pinMode(pin, direction) GPIO::open(pin, direction)
#define delay(milisec) __msleep(milisec)
#define delayMicroseconds(usec) __usleep(usec)
#define millis() __millis()

#endif // __ARCH_CONFIG_H__
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
