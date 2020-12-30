---
title: RF24Revamped.h


---

# RF24Revamped.h


 [More...](#detailed-description)






## Classes

|                | Name           |
| -------------- | -------------- |
| class | **[RF24](/Classes/classRF24/)** <br>Driver class for nRF24L01(+) 2.4GHz Wireless Transceiver.  |

## Types

|                | Name           |
| -------------- | -------------- |
| enum | **[rf24_pa_dbm_e](/Files/RF24Revamped_8h/#enum-rf24_pa_dbm_e)** { RF24_PA_MIN = 0, RF24_PA_LOW, RF24_PA_HIGH, RF24_PA_MAX, RF24_PA_ERROR } |
| enum | **[rf24_datarate_e](/Files/RF24Revamped_8h/#enum-rf24_datarate_e)** { RF24_1MBPS = 0, RF24_2MBPS, RF24_250KBPS } |








## Detailed Description



























Class declaration for [RF24](/Classes/classRF24/) and helper enums 



## Types Documentation

### enum rf24_pa_dbm_e


| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| RF24_PA_MIN | 0 |  (0) represents:  
nRF24L01 | Si24R1 with `lnaEnabled` = 1 | Si24R1 with `lnaEnabled` = 0
-------- | -------------- | --------------
-18 dBm  |  -6 dBm        |  -12 dBm
  |
| RF24_PA_LOW |  |  (1) represents:  
nRF24L01 | Si24R1 with `lnaEnabled` = 1 | Si24R1 with `lnaEnabled` = 0
-------- | -------------- | --------------
-12 dBm  |  0 dBm         |    -4 dBm
  |
| RF24_PA_HIGH |  |  (2) represents:  
nRF24L01 | Si24R1 with `lnaEnabled` = 1 | Si24R1 with `lnaEnabled` = 0
-------- | -------------- | --------------
-6 dBm   |    3 dBm       |    1 dBm
  |
| RF24_PA_MAX |  |  (3) represents:  
nRF24L01 | Si24R1 with `lnaEnabled` = 1 | Si24R1 with `lnaEnabled` = 0
-------- | -------------- | --------------
 0 dBm   |   7 dBm        |    4 dBm
  |
| RF24_PA_ERROR |  |  (4) This should not be used and remains for backward compatibility.  |









**See**: [RF24::setPaLevel()](/Classes/classRF24/#function-setpalevel), [RF24::getPaLevel()](/Classes/classRF24/#function-getpalevel)




















Power Amplifier level. The units dBm (decibel-milliwatts or dB<sub>mW</sub>) represents a logarithmic signal loss. 


### enum rf24_datarate_e


| Enumerator | Value | Description |
| ---------- | ----- | ----------- |
| RF24_1MBPS | 0 |  (0) represents 1 Mbps  |
| RF24_2MBPS |  |  (1) represents 2 Mbps  |
| RF24_250KBPS |  |  (2) represents 250 kbps  |









**See**: [RF24::setDataRate()](/Classes/classRF24/#function-setdatarate), [RF24::getDataRate()](/Classes/classRF24/#function-getdatarate)




















How fast data moves through the air. Units are in bits per second (bps). 







## Source code

```cpp
/*
 Copyright (C) 2011 J. Coliz <maniacbug@ymail.com>

 This program is free software; you can redistribute it and/or
 modify it under the terms of the GNU General Public License
 version 2 as published by the Free Software Foundation.
 */

#ifndef __RF24REVAMPED_H__
#define __RF24REVAMPED_H__

#include "RF24_config.h"

#if defined (RF24_LINUX) || defined (LITTLEWIRE)
    #include "utility/includes.h"
#elif defined SOFTSPI
    #include <DigitalIO.h>
#endif


typedef enum {
    RF24_PA_MIN = 0,

    RF24_PA_LOW,

    RF24_PA_HIGH,

    RF24_PA_MAX,
    RF24_PA_ERROR
} rf24_pa_dbm_e;

typedef enum {
    RF24_1MBPS = 0,
    RF24_2MBPS,
    RF24_250KBPS
} rf24_datarate_e;

class RF24 {
private:
    #ifdef SOFTSPI
    SoftSPI<SOFT_SPI_MISO_PIN, SOFT_SPI_MOSI_PIN, SOFT_SPI_SCK_PIN, SPI_MODE> spi;
    #elif defined (SPI_UART)
    SPIUARTClass uspi;
    #endif

    #if defined (RF24_LINUX) || defined (XMEGA_D3) /* XMEGA can use SPI class */
    SPI spi;
    #endif
    #if defined (MRAA)
    GPIO gpio;
    #endif

    uint16_t ce_pin; 
    uint16_t csn_pin; 
    uint32_t spi_speed; 
    #if defined (RF24_LINUX) || defined (XMEGA_D3)
    uint8_t spi_rxbuff[96+1] ; //SPI receive buffer (payload max 32 bytes)
    uint8_t spi_txbuff[32+1] ; //SPI transmit buffer (payload max 32 bytes + 1 byte for the command)
    #endif
    uint8_t status; 
    uint8_t payload_size[6]; 
    uint8_t open_pipes; 
    uint8_t auto_ack_enabled; 
    uint8_t dyn_pl_enabled; 
    uint8_t feature_reg; 
    uint8_t pipe0_reading_address[5]; 
    uint8_t addr_width; 
    uint8_t config_reg; 
    bool _is_p_variant; 
protected:
    inline void beginTransaction();

    inline void endTransaction();

    void csn(bool mode);

    void read_register(uint8_t reg, uint8_t* buf, uint8_t len);

    uint8_t read_register(uint8_t reg);

    void write_register(uint8_t reg, const uint8_t* buf, uint8_t len);

    void write_register(uint8_t reg, uint8_t value, bool is_cmd_only = false);

public:

    RF24(uint16_t _cepin, uint16_t _cspin, uint32_t _spispeed = RF24_SPI_SPEED);

    #if defined (RF24_LINUX)
    virtual ~RF24() {};
    #endif

    bool begin(void);

    bool isChipConnected();

    void startListening(void);

    void stopListening(void);

    bool available(void);

    void read(void* buf, uint8_t len);

    void openWritingPipe(const uint8_t* address);

    void openReadingPipe(uint8_t number, const uint8_t* address);

    void printDetails(void);

    bool isFifo(bool about_tx, bool check_empty);

    uint8_t isFifo(bool about_tx);

    void powerDown(void);

    void powerUp(void);

    bool send(const void* buf, uint8_t len, const bool multicast=0);

    bool writeAck(uint8_t pipe, const void* buf, uint8_t len);

    void clearStatusFlags(bool dataReady=true, bool dataSent=true, bool dataFail=true);

    bool write(const void* buf, uint8_t len, const bool multicast=0, bool write_only=0);

    bool resend();

    void flushTx(void);

    void flushRx(void);

    bool testRpd(void);

    bool isValid()
    {
        return ce_pin != 0xff && csn_pin != 0xff;
    }

    void closeReadingPipe(uint8_t pipe);

    void setAddressLength(uint8_t length);

    bool getAddressLength(void);

    void setAutoRetry(uint16_t delay, uint8_t count);

    void getAutoRetry(uint16_t* delay, uint8_t* count);

    void setArd(uint16_t delay);

    uint16_t getArd(void);

    void setArc(uint8_t count);

    uint8_t getArc(void);

    void setChannel(uint8_t channel);

    uint8_t getChannel(void);

    void setPayloadLength(uint8_t size);

    void setPayloadLength(uint8_t size, uint8_t pipe);

    uint8_t getPayloadLength(uint8_t pipe=0);

    uint8_t any(void);

    void enableAckPayload(void);

    void disableAckPayload(void);

    void setDynamicPayloads(bool enable);

    void setDynamicPayloadsBin(uint8_t binary_enable);

    void setDynamicPayloads(bool enable, uint8_t pipe);

    bool getDynamicPayloads(uint8_t pipe);

    uint8_t getDynamicPayloads(void);

    void allowMulticast(bool);

    bool isAllowMulticast(void);

    bool isPVariant(void);

    void setAutoAck(bool enable);

    void setAutoAckBin(uint8_t binary_enable);

    void setAutoAck(bool enable, uint8_t pipe);

    bool getAutoAck(uint8_t pipe=0);

    uint8_t getAutoAckBin(void);

    void setPaLevel(uint8_t level, bool lnaEnable=1);

    uint8_t getPaLevel(void);

    uint8_t lastTxArc(void);

    void setDataRate(rf24_datarate_e speed);

    rf24_datarate_e getDataRate(void);

    void setCrc(uint8_t length);

    uint8_t getCrc(void);

    uint8_t update(void);


    bool irqDr(void);

    bool irqDs(void);

    bool irqDf(void);

    bool isTxFull(void);

    uint8_t pipe(void);

    void interruptConfig(bool dataReady=true, bool dataSent=true, bool dataFail=true);

    uint32_t txDelay;

    uint32_t csDelay;

    void startCarrierWave(void);

    void stopCarrierWave(void);

    void openReadingPipe(uint8_t number, uint64_t address);

    void openWritingPipe(uint64_t address);

    void ce(bool level);

private:

    void write_payload(const void* buf, uint8_t len, const uint8_t writeType);

    void read_payload(void* buf, uint8_t len);

    #if !defined (MINIMAL)

    void print_byte_register(const char* name, uint8_t reg, uint8_t qty = 1);

    void print_address_register(const char* name, uint8_t reg, uint8_t qty = 1);

    #endif

    void toggle_features(void);

};
#endif // __RF24_H__
```


-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
