---
title: printf.h


---

# printf.h


 [More...](#detailed-description)










## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[printf_begin](/Files/printf_8h/#function-printf_begin)**(void )  |





## Detailed Description



























Setup necessary to direct stdout to the Arduino Serial library, which enables 'printf' 




## Functions Documentation

### function printf_begin

```cpp
void printf_begin(
    void 
)
```

































## Source code

```cpp
/*
 Copyright (C) 2011 J. Coliz <maniacbug@ymail.com>

 This program is free software; you can redistribute it and/or
 modify it under the terms of the GNU General Public License
 version 2 as published by the Free Software Foundation.
 */
/*  Galileo support from spaniakos <spaniakos@gmail.com> */

#ifndef __PRINTF_H__
#define __PRINTF_H__

#if defined(ARDUINO_ARCH_AVR) || defined(__ARDUINO_X86__)

int serial_putc(char c, FILE *)
{
  Serial.write(c);
  return c;
}
#endif

void printf_begin(void)
{
    #if defined(ARDUINO_ARCH_AVR)
    fdevopen(&serial_putc, 0);

    #elif defined(__ARDUINO_X86__)
    // JESUS - For reddirect stdout to /dev/ttyGS0 (Serial Monitor port)
    stdout = freopen("/dev/ttyGS0", "w", stdout);
    delay(500);
    printf("Redirecting to Serial...");
    #endif // defined(__ARDUINO_X86__)
}

#endif // __PRINTF_H__
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
