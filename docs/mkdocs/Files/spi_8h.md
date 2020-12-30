---
title: utility/Template/spi.h


---

# utility/Template/spi.h


 [More...](#detailed-description)





## Namespaces

| Name           |
| -------------- |
| **[std](/Namespaces/namespacestd/)**  |

## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[SPI](/Classes/classSPI/)**  |









## Detailed Description



























Class declaration for [SPI](/Classes/classSPI/) helper files 








## Source code

```cpp

#include <string>
#include <stdint.h>
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
#include <getopt.h>
#include <fcntl.h>
#include <sys/ioctl.h>
#include <inttypes.h>
#include <linux/types.h>
#include <linux/spi/spidev.h>

using namespace std;

class SPI {
public:

    SPI();

    void begin(int busNo);

    uint8_t transfer(uint8_t tx_);

    void transfernb(char* tbuf, char* rbuf, uint32_t len);

    void transfern(char* buf, uint32_t len);

    virtual ~ SPI();

private:

    string device;
    uint8_t mode;
    uint8_t bits;
    uint32_t speed;
    int fd;

    void init();

};
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
