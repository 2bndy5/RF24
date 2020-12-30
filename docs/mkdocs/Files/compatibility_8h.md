---
title: utility/Template/compatibility.h


---

# utility/Template/compatibility.h


 [More...](#detailed-description)










## Functions

|                | Name           |
| -------------- | -------------- |
| void | **[__msleep](/Files/compatibility_8h/#function-__msleep)**(int milisec)  |
| void | **[__usleep](/Files/compatibility_8h/#function-__usleep)**(int milisec)  |
| void | **[__start_timer](/Files/compatibility_8h/#function-__start_timer)**()  |
| long | **[__millis](/Files/compatibility_8h/#function-__millis)**()  |





## Detailed Description



























Class declaration for [SPI](/Classes/classSPI/) helper files 




## Functions Documentation

### function __msleep

```cpp
void __msleep(
    int milisec
)
```





























### function __usleep

```cpp
void __usleep(
    int milisec
)
```





























### function __start_timer

```cpp
void __start_timer()
```





























### function __millis

```cpp
long __millis()
```

































## Source code

```cpp
/*
 * File:   compatiblity.h
 * Author: purinda
 *
 * Created on 24 June 2012, 3:08 PM
 */

#ifndef COMPATIBLITY_H
#define COMPATIBLITY_H

#ifdef __cplusplus
extern "C" {
#endif

#include <stddef.h>
#include <time.h>
#include <sys/time.h>

void __msleep(int milisec);

void __usleep(int milisec);

void __start_timer();

long __millis();

#ifdef    __cplusplus
}
#endif

#endif    /* COMPATIBLITY_H */
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
