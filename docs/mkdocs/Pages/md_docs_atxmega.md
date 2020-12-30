---
title: ATXMEGA


---

# ATXMEGA


The [RF24](/Classes/classRF24/) driver can be build as a static library with Atmel Studio 7 in order to be included as any other library in another program for the XMEGA family.

Currently only the **ATXMEGA D3** family is implemented.


# Preparation

Create an empty GCC Static Library project in AS7.

As not all files are required, copy the following directory structure in the project:



```cpp
utility\
ATXMegaD3\
    compatibility.c
    compatibility.h
    gpio.cpp
    gpio.h
    gpio_helper.c
    gpio_helper.h
    includes.h
    RF24_arch_config.h
    spi.cpp
    spi.h
nRF24L01.h
printf.h
RF24.cpp
RF24.h
RF24_config.h
```

_Filename: .text_


# Usage

Add the library to your project!

In the file where the `main()` is put the following in order to update the millisecond functionality:



```cpp
ISR(TCE0_OVF_vect)
{
    update_milisec();
}
```

_Filename: .cpp_

Declare the rf24 radio with `[RF24](/Classes/classRF24/) radio(XMEGA_PORTC_PIN3, XMEGA_SPI_PORT_C);`

First parameter is the CE pin which can be any available pin on the uC.

Second parameter is the CS which can be on port C (`XMEGA_SPI_PORT_C`) or on port D (`XMEGA_SPI_PORT_D`).

Call the `[__start_timer()](/Files/compatibility_8h/#function-__start_timer)` to start the millisecond timer.



```
Note about the millisecond functionality:

The millisecond functionality is based on the TCE0 so don't use these pins as IO.
```


The operating frequency of the uC is 32MHz. If you have other frequency change the TCE0 registers appropriatly in function `[__start_timer()](/Files/compatibility_8h/#function-__start_timer)` in _compatibility.c_ file for your frequency. 

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
