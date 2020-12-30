---
title: SPI


---

# SPI






`#include <spi.h>`















## Public Functions

|                | Name           |
| -------------- | -------------- |
|  | **[SPI](/Classes/classSPI/#function-spi)**()  |
| void | **[begin](/Classes/classSPI/#function-begin)**(int busNo)  |
| uint8_t | **[transfer](/Classes/classSPI/#function-transfer)**(uint8_t tx_)  |
| void | **[transfernb](/Classes/classSPI/#function-transfernb)**(char * tbuf, char * rbuf, uint32_t len)  |
| void | **[transfern](/Classes/classSPI/#function-transfern)**(char * buf, uint32_t len)  |
| virtual  | **[~ SPI](/Classes/classSPI/#function-~-spi)**()  |





















## Public Functions Documentation

### function SPI

```cpp
SPI()
```



























[SPI](/Classes/classSPI/) constructor 


### function begin

```cpp
void begin(
    int busNo
)
```



























Start [SPI](/Classes/classSPI/)


### function transfer

```cpp
uint8_t transfer(
    uint8_t tx_
)
```


**Parameters**: 

  * **tx_** Byte to send 







**Return**: Data returned via spi 



















Transfer a single byte 


### function transfernb

```cpp
void transfernb(
    char * tbuf,
    char * rbuf,
    uint32_t len
)
```


**Parameters**: 

  * **tbuf** Transmit buffer 
  * **rbuf** Receive buffer 
  * **len** Length of the data 


























Transfer a buffer of data 


### function transfern

```cpp
void transfern(
    char * buf,
    uint32_t len
)
```


**Parameters**: 

  * **buf** Pointer to a buffer of data 
  * **len** Length of the data 


























Transfer a buffer of data without an rx buffer 


### function ~ SPI

```cpp
virtual ~ SPI()
```





































-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time