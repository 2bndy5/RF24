---
title: GPIO


---

# GPIO






`#include <gpio.h>`















## Public Functions

|                | Name           |
| -------------- | -------------- |
|  | **[GPIO](/Classes/classGPIO/#function-gpio)**()  |
| virtual  | **[~GPIO](/Classes/classGPIO/#function-~gpio)**()  |
| void | **[open](/Classes/classGPIO/#function-open)**(int port, int DDR)  |
| void | **[close](/Classes/classGPIO/#function-close)**(int port)  |
| int | **[read](/Classes/classGPIO/#function-read)**(int port)  |
| void | **[write](/Classes/classGPIO/#function-write)**(int port, int value)  |




## Public Attributes

|                | Name           |
| -------------- | -------------- |
| const int | **[DIRECTION_OUT](/Classes/classGPIO/#variable-direction_out)**  |
| const int | **[DIRECTION_IN](/Classes/classGPIO/#variable-direction_in)**  |
| const int | **[OUTPUT_HIGH](/Classes/classGPIO/#variable-output_high)**  |
| const int | **[OUTPUT_LOW](/Classes/classGPIO/#variable-output_low)**  |

















## Public Functions Documentation

### function GPIO

```cpp
GPIO()
```





























### function ~GPIO

```cpp
virtual ~GPIO()
```





























### function open

```cpp
static void open(
    int port,
    int DDR
)
```


**Parameters**: 

  * **port** 
  * **DDR** 


























Similar to Arduino [pinMode(pin, mode)](/Files/RF24__arch__config_8h/#define-pinmode); 


### function close

```cpp
static void close(
    int port
)
```


**Parameters**: 

  * **port** 




























### function read

```cpp
static int read(
    int port
)
```


**Parameters**: 

  * **port** 


























Similar to Arduino digitalRead(pin); 


### function write

```cpp
static void write(
    int port,
    int value
)
```


**Parameters**: 

  * **port** 
  * **value** 


























Similar to Arduino [digitalWrite(pin, state)](/Files/RF24__arch__config_8h/#define-digitalwrite); 






## Public Attributes Documentation

### variable DIRECTION_OUT

```cpp
static const int DIRECTION_OUT = 1;
```





























### variable DIRECTION_IN

```cpp
static const int DIRECTION_IN = 0;
```





























### variable OUTPUT_HIGH

```cpp
static const int OUTPUT_HIGH = 1;
```





























### variable OUTPUT_LOW

```cpp
static const int OUTPUT_LOW = 0;
```

































-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time