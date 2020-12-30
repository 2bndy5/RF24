---
title: utility/Template/gpio.h


---

# utility/Template/gpio.h


 [More...](#detailed-description)






## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[GPIO](/Classes/classGPIO/)**  |









## Detailed Description



























Class declaration for [SPI](/Classes/classSPI/) helper files 








## Source code

```cpp


#include <cstdio>

class GPIO {
public:
    /* Constants */
    static const int DIRECTION_OUT = 1;
    static const int DIRECTION_IN = 0;

    static const int OUTPUT_HIGH = 1;
    static const int OUTPUT_LOW = 0;

    GPIO();

    static void open(int port, int DDR);

    static void close(int port);

    static int read(int port);

    static void write(int port, int value);

    virtual ~GPIO();
};
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
