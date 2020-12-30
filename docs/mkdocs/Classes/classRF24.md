---
title: RF24
summary: Driver class for nRF24L01(+) 2.4GHz Wireless Transceiver.  

---

# RF24




Driver class for nRF24L01(+) 2.4GHz Wireless Transceiver. 

`#include <RF24Revamped.h>`















## Public Functions

|                | Name           |
| -------------- | -------------- |
|  | **[RF24](/Classes/classRF24/#function-rf24)**(uint16_t _cepin, uint16_t _cspin, uint32_t _spispeed =[RF24_SPI_SPEED](/Files/RF24__config_8h/#define-rf24_spi_speed)) <br>Creates a new instance of this driver.  |
| virtual  | **[~RF24](/Classes/classRF24/#function-~rf24)**()  |
| bool | **[begin](/Classes/classRF24/#function-begin)**(void )  |
| bool | **[isChipConnected](/Classes/classRF24/#function-ischipconnected)**()  |
| void | **[startListening](/Classes/classRF24/#function-startlistening)**(void )  |
| void | **[stopListening](/Classes/classRF24/#function-stoplistening)**(void )  |
| bool | **[available](/Classes/classRF24/#function-available)**(void )  |
| void | **[read](/Classes/classRF24/#function-read)**(void * buf, uint8_t len)  |
| void | **[openWritingPipe](/Classes/classRF24/#function-openwritingpipe)**(const uint8_t * address)  |
| void | **[openReadingPipe](/Classes/classRF24/#function-openreadingpipe)**(uint8_t number, const uint8_t * address)  |
| void | **[printDetails](/Classes/classRF24/#function-printdetails)**(void )  |
| bool | **[isFifo](/Classes/classRF24/#function-isfifo)**(bool about_tx, bool check_empty)  |
| uint8_t | **[isFifo](/Classes/classRF24/#function-isfifo)**(bool about_tx)  |
| void | **[powerDown](/Classes/classRF24/#function-powerdown)**(void )  |
| void | **[powerUp](/Classes/classRF24/#function-powerup)**(void )  |
| bool | **[send](/Classes/classRF24/#function-send)**(const void * buf, uint8_t len, const bool multicast =0)  |
| bool | **[writeAck](/Classes/classRF24/#function-writeack)**(uint8_t pipe, const void * buf, uint8_t len)  |
| void | **[clearStatusFlags](/Classes/classRF24/#function-clearstatusflags)**(bool dataReady =true, bool dataSent =true, bool dataFail =true)  |
| bool | **[write](/Classes/classRF24/#function-write)**(const void * buf, uint8_t len, const bool multicast =0, bool write_only =0)  |
| bool | **[resend](/Classes/classRF24/#function-resend)**()  |
| void | **[flushTx](/Classes/classRF24/#function-flushtx)**(void )  |
| void | **[flushRx](/Classes/classRF24/#function-flushrx)**(void )  |
| bool | **[testRpd](/Classes/classRF24/#function-testrpd)**(void )  |
| bool | **[isValid](/Classes/classRF24/#function-isvalid)**()  |
| void | **[closeReadingPipe](/Classes/classRF24/#function-closereadingpipe)**(uint8_t pipe)  |
| void | **[setAddressLength](/Classes/classRF24/#function-setaddresslength)**(uint8_t length)  |
| bool | **[getAddressLength](/Classes/classRF24/#function-getaddresslength)**(void )  |
| void | **[setAutoRetry](/Classes/classRF24/#function-setautoretry)**(uint16_t delay, uint8_t count)  |
| void | **[getAutoRetry](/Classes/classRF24/#function-getautoretry)**(uint16_t * delay, uint8_t * count)  |
| void | **[setArd](/Classes/classRF24/#function-setard)**(uint16_t delay)  |
| uint16_t | **[getArd](/Classes/classRF24/#function-getard)**(void )  |
| void | **[setArc](/Classes/classRF24/#function-setarc)**(uint8_t count)  |
| uint8_t | **[getArc](/Classes/classRF24/#function-getarc)**(void )  |
| void | **[setChannel](/Classes/classRF24/#function-setchannel)**(uint8_t channel)  |
| uint8_t | **[getChannel](/Classes/classRF24/#function-getchannel)**(void )  |
| void | **[setPayloadLength](/Classes/classRF24/#function-setpayloadlength)**(uint8_t size)  |
| void | **[setPayloadLength](/Classes/classRF24/#function-setpayloadlength)**(uint8_t size, uint8_t pipe)  |
| uint8_t | **[getPayloadLength](/Classes/classRF24/#function-getpayloadlength)**(uint8_t pipe =0)  |
| uint8_t | **[any](/Classes/classRF24/#function-any)**(void )  |
| void | **[enableAckPayload](/Classes/classRF24/#function-enableackpayload)**(void )  |
| void | **[disableAckPayload](/Classes/classRF24/#function-disableackpayload)**(void )  |
| void | **[setDynamicPayloads](/Classes/classRF24/#function-setdynamicpayloads)**(bool enable)  |
| void | **[setDynamicPayloadsBin](/Classes/classRF24/#function-setdynamicpayloadsbin)**(uint8_t binary_enable)  |
| void | **[setDynamicPayloads](/Classes/classRF24/#function-setdynamicpayloads)**(bool enable, uint8_t pipe)  |
| bool | **[getDynamicPayloads](/Classes/classRF24/#function-getdynamicpayloads)**(uint8_t pipe)  |
| uint8_t | **[getDynamicPayloads](/Classes/classRF24/#function-getdynamicpayloads)**(void )  |
| void | **[allowMulticast](/Classes/classRF24/#function-allowmulticast)**(bool enable)  |
| bool | **[isAllowMulticast](/Classes/classRF24/#function-isallowmulticast)**(void )  |
| bool | **[isPVariant](/Classes/classRF24/#function-ispvariant)**(void )  |
| void | **[setAutoAck](/Classes/classRF24/#function-setautoack)**(bool enable)  |
| void | **[setAutoAckBin](/Classes/classRF24/#function-setautoackbin)**(uint8_t binary_enable)  |
| void | **[setAutoAck](/Classes/classRF24/#function-setautoack)**(bool enable, uint8_t pipe)  |
| bool | **[getAutoAck](/Classes/classRF24/#function-getautoack)**(uint8_t pipe =0)  |
| uint8_t | **[getAutoAckBin](/Classes/classRF24/#function-getautoackbin)**(void )  |
| void | **[setPaLevel](/Classes/classRF24/#function-setpalevel)**(uint8_t level, bool lnaEnable =1)  |
| uint8_t | **[getPaLevel](/Classes/classRF24/#function-getpalevel)**(void )  |
| uint8_t | **[lastTxArc](/Classes/classRF24/#function-lasttxarc)**(void )  |
| void | **[setDataRate](/Classes/classRF24/#function-setdatarate)**([rf24_datarate_e](/Files/RF24Revamped_8h/#enum-rf24_datarate_e) speed)  |
| [rf24_datarate_e](/Files/RF24Revamped_8h/#enum-rf24_datarate_e) | **[getDataRate](/Classes/classRF24/#function-getdatarate)**(void )  |
| void | **[setCrc](/Classes/classRF24/#function-setcrc)**(uint8_t length)  |
| uint8_t | **[getCrc](/Classes/classRF24/#function-getcrc)**(void )  |
| uint8_t | **[update](/Classes/classRF24/#function-update)**(void )  |
| bool | **[irqDr](/Classes/classRF24/#function-irqdr)**(void )  |
| bool | **[irqDs](/Classes/classRF24/#function-irqds)**(void )  |
| bool | **[irqDf](/Classes/classRF24/#function-irqdf)**(void )  |
| bool | **[isTxFull](/Classes/classRF24/#function-istxfull)**(void )  |
| uint8_t | **[pipe](/Classes/classRF24/#function-pipe)**(void )  |
| void | **[interruptConfig](/Classes/classRF24/#function-interruptconfig)**(bool dataReady =true, bool dataSent =true, bool dataFail =true)  |
| void | **[startCarrierWave](/Classes/classRF24/#function-startcarrierwave)**(void )  |
| void | **[stopCarrierWave](/Classes/classRF24/#function-stopcarrierwave)**(void )  |
| void | **[openReadingPipe](/Classes/classRF24/#function-openreadingpipe)**(uint8_t number, uint64_t address)  |
| void | **[openWritingPipe](/Classes/classRF24/#function-openwritingpipe)**(uint64_t address)  |
| void | **[ce](/Classes/classRF24/#function-ce)**(bool level)  |

## Protected Functions

|                | Name           |
| -------------- | -------------- |
| void | **[beginTransaction](/Classes/classRF24/#function-begintransaction)**()  |
| void | **[endTransaction](/Classes/classRF24/#function-endtransaction)**()  |
| void | **[csn](/Classes/classRF24/#function-csn)**(bool mode)  |
| void | **[read_register](/Classes/classRF24/#function-read_register)**(uint8_t reg, uint8_t * buf, uint8_t len)  |
| uint8_t | **[read_register](/Classes/classRF24/#function-read_register)**(uint8_t reg)  |
| void | **[write_register](/Classes/classRF24/#function-write_register)**(uint8_t reg, const uint8_t * buf, uint8_t len)  |
| void | **[write_register](/Classes/classRF24/#function-write_register)**(uint8_t reg, uint8_t value, bool is_cmd_only =false)  |



## Public Attributes

|                | Name           |
| -------------- | -------------- |
| uint32_t | **[txDelay](/Classes/classRF24/#variable-txdelay)**  |
| uint32_t | **[csDelay](/Classes/classRF24/#variable-csdelay)**  |

















## Public Functions Documentation

### function RF24

```cpp
RF24(
    uint16_t _cepin,
    uint16_t _cspin,
    uint32_t _spispeed =RF24_SPI_SPEED
)
```

Creates a new instance of this driver. 

**Parameters**: 

  * **_cepin** The pin attached to Chip Enable on the RF module 
  * **_cspin** The pin attached to Chip Select 
  * **_spispeed** The [SPI](/Classes/classSPI/) speed in Hz ie: 1000000 == 1Mhz 












**Note**: Users can specify default [SPI](/Classes/classSPI/) speed by modifying `#define RF24_SPI_SPEED` in [RF24_config.h](/Files/RF24__config_8h/#file-rf24_config.h) For Arduino, [SPI](/Classes/classSPI/) speed will only be properly configured this way on devices supporting [SPI](/Classes/classSPI/) TRANSACTIONS. Older/Unsupported Arduino devices will use a default clock divider and settings configuration Linux: The old way of setting [SPI](/Classes/classSPI/) speeds using BCM2835 driver enums has been removed 














[RF24](/Classes/classRF24/) Constructor

Before using, you create an instance and send in the unique pins that this chip is connected to.

See [Arduino](/Pages/md_docs_arduino/#page-md_docs_arduino), [ATTiny](/Pages/md_docs_attiny/#page-md_docs_attiny), or [Linux](/Pages/md_docs_rpi_general/#page-md_docs_rpi_general) pages for device specific information.


### function ~RF24

```cpp
inline virtual ~RF24()
```





























### function begin

```cpp
bool begin(
    void 
)
```








**Return**: 

* `true` if the radio is not responding to [SPI](/Classes/classSPI/) transactions
* `false` if the radio is responsive to [SPI](/Classes/classSPI/) transactions 



















Begin operation of the chip

Call this in setup(), before calling any other methods. !!! important Use this function to determine if there is a hardware problem before continuing application. ```cpp if (!radio.[begin()](/Classes/classRF24/#function-begin)) { // if the radio is unresponsive? while (1) {} // hold in infinite loop } ``` 


### function isChipConnected

```cpp
bool isChipConnected()
```



























Checks if the chip is connected to the [SPI](/Classes/classSPI/) bus 


### function startListening

```cpp
void startListening(
    void 
)
```













**Note**: 

```
If there was a call to :func:`openReadingPipe()` about pipe 0 prior to
calling this function, then this function will re-write the address
that was last set to reading pipe 0. This is because :func:`openWritingPipe()`
will overwrite the address to reading pipe 0 for proper auto-ack
functionality.
```














Start listening on the pipes opened for reading.



1. Be sure to call [openReadingPipe()](/Classes/classRF24/#function-openreadingpipe) first.
2. Do not call [send()](/Classes/classRF24/#function-send) while in this mode, without first calling [stopListening()](/Classes/classRF24/#function-stoplistening).
3. Call [available()](/Classes/classRF24/#function-available) to check for incoming traffic, and [read()](/Classes/classRF24/#function-read) to get it.
Open reading pipe 1 using address `0xCCCECCCECC`

```cpp
 {c++}
byte address[] = {0xCC, 0xCE, 0xCC, 0xCE, 0xCC};
radio.openReadingPipe(1,address);
radio.startListening();
```


### function stopListening

```cpp
void stopListening(
    void 
)
```













**Note**: 

```
When the ACK payloads feature is enabled, the TX FIFO buffers are
flushed when calling this function. This is meant to discard any ACK
payloads that were not appended to acknowledgment packets.
```














Stop listening for incoming messages, and switch to transmit mode.

Do this before calling [send()](/Classes/classRF24/#function-send). 

```cpp
radio.stopListening();
radio.send(&data, sizeof(data));
```

_Filename: .cpp_


### function available

```cpp
bool available(
    void 
)
```







**See**: [any()](/Classes/classRF24/#function-any)

**Return**: 

* true if there is a payload available in the RX FIFO buffers
* false if there is no payload available in the RX FIFO buffers



















Check whether there are bytes available to be read 

```cpp
if(radio.available()){
  radio.read(&data, sizeof(data));
}
```

_Filename: .cpp_


!!! warning 

```
This function relies on the information about the pipe number
that received the next available payload. According to the datasheet,
the data about the pipe number that received the next available payload
is "unreliable" during a FALLING transition on the IRQ pin. This means
you should call clearStatusFlags() before calling this function
during an ISR (Interrupt Service Routine).

For example:
```cpp
void isrCallbackFunction() {
  radio.clearStatusFlags(); // resets the IRQ pin to HIGH
  radio.available();        // returned data should now be reliable
}

void setup() {
  pinMode(IRQ_PIN, INPUT);
  attachInterrupt(digitalPinToInterrupt(IRQ_PIN), isrCallbackFunction, FALLING);
}
```
```


### function read

```cpp
void read(
    void * buf,
    uint8_t len
)
```


**Parameters**: 

  * **buf** Pointer to a buffer where the data should be written 
  * **len** Maximum number of bytes to read into the buffer. This value should match the length of the object referenced using the `buf` parameter. The absolute maximum number of bytes that can be read in one call is 96. !!! hint 

```
Remember that each call to read() fetches data from the
RX FIFO beginning with the first byte from the first available
payload. A payload is not removed from the RX FIFO until it's
entire length (or more) is fetched using read().
```












**Note**: 

```
`void*` was chosen specifically as a data type to make it easier
for beginners to use (no casting needed).
```














Read payload data from the RX FIFO buffer(s).

The length of data read is usually the next available payload's length 

* If `len` parameter's value is less than the available payload's length, then the payload remains in the RX FIFO.
* If `len` parameter's value is greater than the first of multiple available payloads, then the data saved to the `buf` parameter's object will be supplemented with data from the next available payload.
* If `len` parameter's value is greater than the last available payload's length, then the last byte in the payload is used as padding for the data saved to the `buf` parameter's object. The nRF24L01 will repeatedly use the last byte from the last payload even when [read()](/Classes/classRF24/#function-read) is called with an empty RX FIFO. [any()](/Classes/classRF24/#function-any), [available()](/Classes/classRF24/#function-available)


### function openWritingPipe

```cpp
void openWritingPipe(
    const uint8_t * address
)
```


**Parameters**: 

  * **address** The address to be used for outgoing transmissions (uses pipe 0). Coordinate this address amongst other receiving nodes (the pipe numbers don't need to match). 






**See**: [setAddressLength()](/Classes/classRF24/#function-setaddresslength), [startListening()](/Classes/classRF24/#function-startlistening)






**Note**: 

```
There is no address length parameter because this function will
always write the number of bytes that the radio addresses are configured
to use (set with :func:`setAddressLength()`).
```














New: Open a pipe for writing via byte array. Old addressing format retained for compatibility.

Only one writing pipe can be opened at once, but this function changes the address that is used to transmit (ACK payloads/packets do not apply here). Be sure to call [stopListening()](/Classes/classRF24/#function-stoplistening) prior to calling this function.

Addresses are assigned via a byte array, default is 5 byte address length 

```cpp
uint8_t addresses[][6] = {"1Node", "2Node"};
radio.openWritingPipe(addresses[0]);
```

_Filename: .cpp_



```cpp
uint8_t address[] = {0xCC, 0xCE, 0xCC, 0xCE, 0xCC};
radio.openWritingPipe(address);
address[0] = 0x33;
radio.openReadingPipe(1, address);
```

_Filename: .cpp_

!!! warning 

```
This function will overwrite the address set to reading pipe 0
as stipulated by the datasheet for proper auto-ack functionality in TX
mode. Use this function to ensure proper transmission acknowledgement
when the address set to reading pipe 0 (via :func:`openReadingPipe()`) does
not match the address passed to this function. If the auto-ack feature is
disabled, then this function will still overwrite the address for
reading pipe 0 regardless.
```


### function openReadingPipe

```cpp
void openReadingPipe(
    uint8_t number,
    const uint8_t * address
)
```


**Parameters**: 

  * **number** Which pipe to open. Only pipe numbers 0-5 are available, an address assigned to any pipe number not in that range will be ignored. 
  * **address** The 3, 4, or 5 byte address to assign to an RX pipe. 






**See**: [openWritingPipe()](/Classes/classRF24/#function-openwritingpipe), [setAddressLength()](/Classes/classRF24/#function-setaddresslength)






**Note**: 

  * 

```
Pipes 0 and 1 will store a full 5-byte address. Pipes 2-5 will
technically only store a single byte, borrowing up to 4 additional bytes
from pipe 1 per the assigned address width.

Pipes 1-5 should share the same address, except the first byte.
Only the first byte in the array should be unique, e.g.
```cpp
uint8_t addresses[][6] = {"Prime", "2Node", "3xxxx", "4xxxx"};
openReadingPipe(0, addresses[0]); // address used is "Prime"
openReadingPipe(1, addresses[1]); // address used is "2Node"
openReadingPipe(2, addresses[2]); // address used is "3Node"
openReadingPipe(3, addresses[3]); // address used is "4Node"
```
```

 !!! warning 

```
If the reading pipe 0 is opened by this function, the address
passed to this function (for pipe 0) will be restored at every call to
:func:`startListening()`, but the address for pipe 0 is ONLY restored
if the LSB is a non-zero value.

Read `this article <http://maniacalbits.blogspot.com/2013/04/rf24-addressing-nrf24l01-radios-require.html>`_
to understand how to avoid using malformed addresses. This address
restoration is implemented because of the underlying neccessary
functionality of :func:`openWritingPipe()`.
```
  * 

```
There is no address length parameter because this function will
always write the number of bytes (for pipes 0 and 1) that the radio
addresses are configured to use (set with :func:`setAddressLength()`).
```















Open a pipe for reading

Up to 6 pipes can be open for reading at once. Open all the required reading pipes, and then call [startListening()](/Classes/classRF24/#function-startlistening).


### function printDetails

```cpp
void printDetails(
    void 
)
```













**Note**: 

```
If the automatic acknowledgements feature is configured differently
for each pipe, then a binary representation is used in which bits 0-5
represent pipes 0-5 respectively. A `0` means the feature is disabled and
a `1` means the feature is enabled.
```














Print a giant block of debugging information to stdout. Only use this function if your application can spare extra bytes of memory. !!! warning 

```
Does nothing if stdout is not defined. See fdevopen in stdio.h
The printf.h file is included with the library for Arduino.
```cpp
#include "printf.h"
setup() {
  Serial.begin(115200);
  printf_begin();
  // ...
}
```
```


### function isFifo

```cpp
bool isFifo(
    bool about_tx,
    bool check_empty
)
```


**Parameters**: 

  * **about_tx** Specify which FIFO the returned data should concern.

* `true` fetches data about the TX FIFO
* `false` fetches data about the RX FIFO 
  * **check_empty** Specify if the data returned about the specified FIFO describes it as empty or full.

* `true` checks if the specified FIFO is empty
* `false` checks if the specified FIFO is full 







**Return**: A boolean that answers the question (according to the parameters)

 Is the [TX or RX] FIFO [empty or full]? 



















Use this function to check if the radio's RX FIFO levels are all occupied. This can be used to prevent data loss because any incoming transmissions are rejected if there is no unoccupied levels in the RX FIFO to store the incoming payload. Remember that each level can hold up to a maximum of 32 bytes. 


### function isFifo

```cpp
uint8_t isFifo(
    bool about_tx
)
```


**Parameters**: 

  * **about_tx** Specify which FIFO the returned data should concern.

* `true` fetches data about the TX FIFO
* `false` fetches data about the RX FIFO 







**Return**: an number consisting of 2 bits where each bit describes the empty and full state of the specified FIFO buffers.

* `2` means the FIFO is full
* `1` means the FIFO is empty
* `0` means the FIFO is neither full nor empty 



















Get 2 binary bits of data about either FIFO buffers. 


### function powerDown

```cpp
void powerDown(
    void 
)
```













**Note**: 

```
After calling startListening(), a basic radio will consume about
13.5mA at max PA level. During active transmission, the radio will consume
about 11.5mA, but this will be reduced to 26uA (.026mA) between sending.
In full powerDown mode, the radio will consume approximately 900nA (.0009mA)
```



```cpp
radio.powerDown();
avr_enter_sleep_mode(); // Custom function to sleep the device
radio.powerUp();
```

_Filename: .cpp_














Enter low-power mode

To return to normal power mode, call [powerUp()](/Classes/classRF24/#function-powerup). 


### function powerUp

```cpp
void powerUp(
    void 
)
```













**Note**: 

```
This will take up to 5ms for maximum compatibility.
```














Leave low-power mode - required for normal radio operation after calling [powerDown()](/Classes/classRF24/#function-powerdown)

To return to low power mode, call [powerDown()](/Classes/classRF24/#function-powerdown). 


### function send

```cpp
bool send(
    const void * buf,
    uint8_t len,
    const bool multicast =0
)
```


**Parameters**: 

  * **buf** Pointer to the data to be sent 
  * **len** Number of bytes to be sent. The maximum size of data from `buf` is 32 bytes (for dynamic payload lengths) or the static payload length specified by [setPayloadLength()](/Classes/classRF24/#function-setpayloadlength). If this parameter is less than what [getPayloadLength()](/Classes/classRF24/#function-getpayloadlength) returns (about pipe 0), then the remainder will be padded with zeroes. 
  * **multicast** Request ACK response (`false`), or no ACK response (`true`). Be sure to have called [allowMulticast()](/Classes/classRF24/#function-allowmulticast) at least once before setting this parameter. 






**See**: [setAutoAck()](/Classes/classRF24/#function-setautoack)

**Return**: 

* `true` if the payload was delivered successfully and an acknowledgement (ACK packet) was received. If auto-ack is disabled, then any attempt to transmit will also return true (even if the payload was not received).
* `false` if the payload was sent but was not acknowledged with an ACK packet. This condition can only be reported if the auto-ack feature is on. 



















This blocks until the message is successfully acknowledged by the receiver or the timeout/retransmit maxima are reached.

Be sure to call [openWritingPipe()](/Classes/classRF24/#function-openwritingpipe) first to set the destination of the paylooad.

The [irqDs()](/Classes/classRF24/#function-irqds) and [irqDf()](/Classes/classRF24/#function-irqdf) interrupt flags will be cleared upon entering this function 


### function writeAck

```cpp
bool writeAck(
    uint8_t pipe,
    const void * buf,
    uint8_t len
)
```


**Parameters**: 

  * **pipe** Which pipe# (typically 1-5) will get this response. 
  * **buf** Pointer to data that is sent 
  * **len** Length of the data to send, up to 32 bytes max. Not affected by the static payload set by [setPayloadLength()](/Classes/classRF24/#function-setpayloadlength). 






**See**: [enableAckPayload()](/Classes/classRF24/#function-enableackpayload), [setDynamicPayloads()](/Classes/classRF24/#function-setdynamicpayloads) !!! important 

```
Dynamic payloads must be enabled.
```

**Return**: 

* `true` if the payload was loaded into the TX FIFO.
* `false` if the payload wasn't loaded into the TX FIFO because it is already full or the ACK payload feature is not enabled using [enableAckPayload()](/Classes/classRF24/#function-enableackpayload). 





**Note**: 

  * 

```
ACK payloads are dynamic payloads. Calling enableAckPayload()
will automatically enable dynamic payloads on pipe 0 (required for TX
mode when expecting ACK payloads). To use ACK payloads on any other
pipe in RX mode, call setDynamicPayloads().
```
  * 

```
ACK payloads are handled automatically by the radio chip when a
regular payload is received. It is important to discard regular payloads
in the TX FIFO (using flushTx()) before loading the first ACK payload
into the TX FIFO. This function can be called before and after calling
startListening().
```

 !!! warning 

```
Only 3 of these ACK payloads can be pending at any time because there
are only 3 FIFO buffers.
```















Write an acknowledgement (ACK) payload for the specified pipe

The next time a message is received on a specified `pipe`, the data in `buf` will be sent back in the ACK payload. 


### function clearStatusFlags

```cpp
void clearStatusFlags(
    bool dataReady =true,
    bool dataSent =true,
    bool dataFail =true
)
```


**Parameters**: 

  * **dataReady** There is a newly received payload (RX_DR) saved to RX FIFO buffers. Remember that the RX FIFO can only hold up to 3 payloads. Once the RX FIFO is full, all further received transmissions are rejected until there is space to save new data in the RX FIFO buffers. 
  * **dataSent** The transmission attempt completed (TX_DS). This does not imply that the transmitted data was received by another radio, rather this only reports if the attempt to send was completed. This will always be `true` when the auto-ack feature is disabled. 
  * **dataFail** The transmission failed to be acknowledged, meaning too many retries (MAX_RT) were made while expecting an ACK packet. This event is only triggered when auto-ack feature is enabled. 






**See**: [interruptConfig()](/Classes/classRF24/#function-interruptconfig)




















Call this when you get an Interrupt Request (IRQ) to find out why

This function describes what event triggered the IRQ pin to go active LOW and clears the status of all events. 


### function write

```cpp
bool write(
    const void * buf,
    uint8_t len,
    const bool multicast =0,
    bool write_only =0
)
```


**Parameters**: 

  * **buf** Pointer to the data to be sent 
  * **len** Number of bytes to be sent 
  * **multicast** Request ACK packet response (`false`), or no ACK packet response (`true`). Be sure to have called [allowMulticast()](/Classes/classRF24/#function-allowmulticast) at least once before setting this parameter. 
  * **write_only** If this is set to `false`, then this function sets the CE pin to active (enabling TX transmissions). `true` has no effect on the CE pin and simply loads the payload into the TX FIFO. 






**See**: [send()](/Classes/classRF24/#function-send), [setAutoAck()](/Classes/classRF24/#function-setautoack), [allowMulticast()](/Classes/classRF24/#function-allowmulticast)

**Return**: 

* `true` if the payload was loaded into the TX FIFO.
* `false` if the payload wasn't loaded into the TX FIFO because it is already full. 





**Note**: 

```
This function leaves the CE pin HIGH, so the radio will remain in TX or
StandBy-II Mode until a ce() is called to set the pin LOW (into
StandBy-I mode). Can be used as an alternative to send() if using
all 3 levels of the TX FIFO  to manage multiple payloads at once.
```

 !!! warning 

```
It is important to never keep the nRF24L01 in TX mode with FIFO full
for more than 4ms at a time. If the auto retransmit/autoAck is enabled, the
nRF24L01 is never in TX mode long enough to disobey this rule. Allow the FIFO
to clear by calling ce() to the the CE pin inactive LOW.
```














Write a payload to the TX FIFO buffers. This function actually serves as a helper to [send()](/Classes/classRF24/#function-send). 


### function resend

```cpp
bool resend()
```








**Return**: 

* `true` if re-transmission was successful.
* `false` if the re-transmission failed or the TX FIFO was already empty. 





**Note**: 

```
This is to be used AFTER auto-retry fails if wanting to resend
using the built-in payload reuse feature. In the event of a
re-transmission failure, simply call this function again to
resume re-transmission of the same payload.
```














The function will instruct the radio to re-use the payload in the top level (first out) of the TX FIFO buffers when a TX failure occurs. The auto-retry feature is applied just like when calling [send()](/Classes/classRF24/#function-send). Calling this function prevents succefully sent payloads from being removed from the TX FIFO buffer until calling [flushTx()](/Classes/classRF24/#function-flushtx). If the TX FIFO has only the one payload (in the top level), the re-used payload can be overwritten by using [send()](/Classes/classRF24/#function-send) or [write()](/Classes/classRF24/#function-write). If the TX FIFO has other payloads enqueued, then using [send()](/Classes/classRF24/#function-send) or [write()](/Classes/classRF24/#function-write) will attempt to enqueue a new payload in the TX FIFO (does not overwrite the top level of the TX FIFO). Currently, [stopListening()](/Classes/classRF24/#function-stoplistening) also calls [flushTx()](/Classes/classRF24/#function-flushtx) when ACK payloads are enabled (via [enableAckPayload()](/Classes/classRF24/#function-enableackpayload)).

This function only applies when taking advantage of the auto-retry feature. See [setAutoAck()](/Classes/classRF24/#function-setautoack) and [setAutoRetry()](/Classes/classRF24/#function-setautoretry) to configure the auto-retry feature. 


### function flushTx

```cpp
void flushTx(
    void 
)
```



























Empty all 3 of the TX (transmit) FIFO buffers. This is automatically called by [stopListening()](/Classes/classRF24/#function-stoplistening) if ACK payloads are enabled. However, [startListening()](/Classes/classRF24/#function-startlistening) does not call this function. 


### function flushRx

```cpp
void flushRx(
    void 
)
```



























Empty all 3 of the RX (receive) FIFO buffers. 


### function testRpd

```cpp
bool testRpd(
    void 
)
```







**See**: [startCarrierWave()](/Classes/classRF24/#function-startcarrierwave), [stopCarrierWave()](/Classes/classRF24/#function-stopcarrierwave)

**Return**: This data is reset upon entering RX mode.

* `true` if a signal with an amplitude of greater than or equal to -64dBm was detected.
* `false` if no signal with an amplitude of greater than or equal to -64 dBm was detected. 



















Test whether a signal (carrier wave or otherwise) greater than or equal to -64dBm is present on the channel. This can be used to check for interference on the current channel and channel hopping strategies. 

```cpp
bool goodSignal = radio.testRpd();
if(radio.available()){
   Serial.println(goodSignal ? "Strong signal > 64dBm" : "Weak signal < 64dBm" );
   radio.read(0, 0);
}
```

_Filename: .cpp_


### function isValid

```cpp
inline bool isValid()
```








**Return**: `true` if this is a legitimate radio, `false` if not. 



















Test whether this is a real radio, or a mock shim for debugging. Setting both CE & CSN pins to `0xFF` is the way to indicate that this is not a real radio. 


### function closeReadingPipe

```cpp
void closeReadingPipe(
    uint8_t pipe
)
```


**Parameters**: 

  * **pipe** Which pipe number to close, any integer not in range [0, 5] is ignored. 


























Close a pipe after it has been previously opened. Can be safely called without having previously opened a pipe. 


### function setAddressLength

```cpp
void setAddressLength(
    uint8_t length
)
```


**Parameters**: 

  * **length** The address length (in bytes) to use; this parameter is clamped to the range [3, 5]. 


























Set the address length from 3 to 5 bytes 


### function getAddressLength

```cpp
bool getAddressLength(
    void 
)
```








**Return**: The address length (in bytes) currently configured by [setAddressLength()](/Classes/classRF24/#function-setaddresslength). This number will be in range [3, 5]. 





















### function setAutoRetry

```cpp
void setAutoRetry(
    uint16_t delay,
    uint8_t count
)
```


**Parameters**: 

  * **delay** How long to wait (in microseconds) between each auto-retry attempt. This parameter is clamped to the range [250, 4000]. The default is 1500 us. 
  * **count** How many auto-retry attempts before giving up. The default and maximum is 15. Use 0 to disable the auto-retry feature all together. 






**See**: [lastTxArc()](/Classes/classRF24/#function-lasttxarc), [setArd()](/Classes/classRF24/#function-setard), [setArc()](/Classes/classRF24/#function-setarc)






**Note**: 

```
Disabling the auto-retry feature on a transmitter still uses the
auto-ack feature (if enabled), except it will not retry to transmit if
the payload was not acknowledged on the first attempt.
```














Set the number of retry attempts and delay between retry attempts when transmitting a payload. The radio is waiting for an acknowledgement (ACK) packet during the delay between retry attempts. 


### function getAutoRetry

```cpp
void getAutoRetry(
    uint16_t * delay,
    uint8_t * count
)
```


**Parameters**: 

  * **delay** The reference variable that will store the amount of microseconds that the radio waits for an acknowledgement (ACK) packet response between auto-retry attempted transmissions. 
  * **count** The reference variable that will store the maximum number of auto-retry attempts allowed. 






**See**: [setAutoRetry()](/Classes/classRF24/#function-setautoretry), [getArd()](/Classes/classRF24/#function-getard), [getArc()](/Classes/classRF24/#function-getarc)

**Return**: This function returns nothing (`void`). All returned data is stored in the referenced variables passed as arguments. 

```cpp
uint16_t autoDelay;
uint8_t autoCount;
radio.getAutoRetry(&autoDelay, &autoCount);
```

_Filename: .cpp_



















Fetch the configuration of the auto-retry feature 


### function setArd

```cpp
void setArd(
    uint16_t delay
)
```


**Parameters**: 

  * **delay** How long to wait (in microseconds) between each auto-retry attempt. This parameter is clamped to the range [250, 4000]. The default is 1500 us. 






**See**: [setAutoRetry()](/Classes/classRF24/#function-setautoretry)




















Configure the auto-retry feature's delay (ARD). 


### function getArd

```cpp
uint16_t getArd(
    void 
)
```







**See**: [setAutoRetry()](/Classes/classRF24/#function-setautoretry), [getAutoRetry()](/Classes/classRF24/#function-getautoretry), [setArd()](/Classes/classRF24/#function-setard)




















Get the auto-retry feature's delay (ARD) configuration, 


### function setArc

```cpp
void setArc(
    uint8_t count
)
```


**Parameters**: 

  * **count** How many auto-retry attempts before giving up. The default and maximum is 15. Use 0 to disable the auto-retry feature all together. 






**See**: [setAutoRetry()](/Classes/classRF24/#function-setautoretry), [lastTxArc()](/Classes/classRF24/#function-lasttxarc)




















Configure the auto-retry feature's count (ARC). 


### function getArc

```cpp
uint8_t getArc(
    void 
)
```







**See**: [setAutoRetry()](/Classes/classRF24/#function-setautoretry), [getAutoRetry()](/Classes/classRF24/#function-getautoretry), [setArc()](/Classes/classRF24/#function-setarc), [lastTxArc()](/Classes/classRF24/#function-lasttxarc)




















Get the auto-retry feature's count (ARC) configuration. 


### function setChannel

```cpp
void setChannel(
    uint8_t channel
)
```


**Parameters**: 

  * **channel** Which RF channel to communicate on. This parameter is clamped to the range [0, 125]. 


























Set RF communication channel. The frequency used by a channel is calculated as:

2400 MHz + <channel number>

Meaning the default channel of 76 uses the approximate frequency of 2476 MHz. 


### function getChannel

```cpp
uint8_t getChannel(
    void 
)
```








**Return**: The currently configured RF Channel 



















Get RF communication channel 


### function setPayloadLength

```cpp
void setPayloadLength(
    uint8_t size
)
```


**Parameters**: 

  * **size** The number of bytes to use for payload lengths handled by all pipes. This parameter is clamped to the range [1, 32]. 


























Set Static Payload length to be expected for all pipes. 


### function setPayloadLength

```cpp
void setPayloadLength(
    uint8_t size,
    uint8_t pipe
)
```


**Parameters**: 

  * **size** The number of bytes to use for payload lengths handled by the pipe specified by the `pipe` parameter. This parameter is clamped to the range [1, 32]. 
  * **pipe** The specific pipe to configure the length for static payloads. 






**See**: [getPayloadLength()](/Classes/classRF24/#function-getpayloadlength), [any()](/Classes/classRF24/#function-any)




















Set Static Payload length to be expected for a specific pipe. 


### function getPayloadLength

```cpp
uint8_t getPayloadLength(
    uint8_t pipe =0
)
```


**Parameters**: 

  * **pipe** the specific pipe about the configuration being fetched. If not specified, then the data returned is about pipe 0. 






**See**: [setPayloadLength(uint8_t, uint8_t)](/Classes/classRF24/#function-setpayloadlength), [setPayloadLength(uint8_t)](/Classes/classRF24/#function-setpayloadlength), [any()](/Classes/classRF24/#function-any)

**Return**: The payload length in bytes that a pipe is configured to use. 



















Get Static Payload length for a specific pipe 


### function any

```cpp
uint8_t any(
    void 
)
```








**Return**: Payload length in bytes of next available payload in the RX FIFO. If no payload is available then this function returns 0. 



















Get next available payload length in bytes. This function is compatible with static or dynamic payloads. 


### function enableAckPayload

```cpp
void enableAckPayload(
    void 
)
```







**See**: [setAutoAck()](/Classes/classRF24/#function-setautoack)






**Note**: 

```
ACK payloads are dynamic payloads. This function automatically
enables dynamic payloads on pipe 0 by default. Call
setDynamicPayloads() to enable on all pipes (especially for RX
nodes that use pipes other than pipe 0 to receive transmissions expecting
responses with ACK payloads).
```














Enable custom payloads in the acknowledge packets

ACK payloads are a handy way to return data back to senders without manually changing the radio modes on both units.

The ACK payload feature requires the auto-ack feature to be enabled for any pipe using ACK payloads. This function does not automatically enable the auto-ack feature on pipe 0 since the auto-ack feature is enabled for all pipes by default. 


### function disableAckPayload

```cpp
void disableAckPayload(
    void 
)
```







**See**: [enableAckPayload()](/Classes/classRF24/#function-enableackpayload)




















Disable custom payloads on the ackowledge packets 


### function setDynamicPayloads

```cpp
void setDynamicPayloads(
    bool enable
)
```


**Parameters**: 

  * **enable** Enable (`true`) or disable (`false`) the dynamic payload length feature for all pipes. 


























Enable or disable dynamically sized payloads for all pipes

If this feature is enabled, then the static payload lengths configuration is not used. 


### function setDynamicPayloadsBin

```cpp
void setDynamicPayloadsBin(
    uint8_t binary_enable
)
```


**Parameters**: 

  * **binary_enable** A binary integer to control the dynamic payload length feature for all pipes. Bit positions 0-5 represent pipes 0-5 respectively. A high bit (`1`) enables the feature for the corresponding pipe; a low bit (`0`) disables the feature for the corresponding pipe. 


























Enable or disable dynamically sized payloads for all pipes using a binary integer.

If this feature is enabled, then the static payload lengths configuration is not used. 


### function setDynamicPayloads

```cpp
void setDynamicPayloads(
    bool enable,
    uint8_t pipe
)
```


**Parameters**: 

  * **enable** the configuration of the dynamic payload length feature concerning specific pipe. 
  * **pipe** the specific pipe concerning the dynamic payload length feature. 


























Enable or disable dynamically sized payloads for a specific pipe.

If this feature is enabled for any pipe, then the static payload length configuration for that pipe is not used. 


### function getDynamicPayloads

```cpp
bool getDynamicPayloads(
    uint8_t pipe
)
```


**Parameters**: 

  * **pipe** the specific pipe concerning the dynamic payload length feature. 


























Get the configuration of dynamically sized payloads for a specific pipe.

If this feature is enabled for any pipe, then the static payload length configuration for that pipe is not used. 


### function getDynamicPayloads

```cpp
uint8_t getDynamicPayloads(
    void 
)
```








**Return**: A binary integer where each bit represents the dynamic payload feature configuration for a specific pipe. Bit position 0 represents pipe 0, and bit position 5 represents pipe 5. A high bit (`1`) enables the feature for the corresponding pipe; a low bit (`0`) disables the feature for the corresponding pipe. Bit position 6 and 7 will always be `0`. 



















Get the configuration of dynamically sized payloads for all pipes.

If this feature is enabled for any pipe, then the static payload length configuration for that pipe is not used. 


### function allowMulticast

```cpp
void allowMulticast(
    bool enable
)
```


**Parameters**: 

  * **enable** Enables (`true`) or disables (`false`) the affect of the `multicast` parameter to [send()](/Classes/classRF24/#function-send) or [write()](/Classes/classRF24/#function-write). 






**See**: [setAutoAck(bool)](/Classes/classRF24/#function-setautoack), [setAutoAck(bool, uint8_t)](/Classes/classRF24/#function-setautoack)






**Note**: 

```
This function must be called once before using the multicast
parameter for any functions that offer it. To use multicast behavior
about all outgoing payloads (using pipe 0) or incoming payloads
(concerning all RX pipes), use setAutoAck().
```














Enable dynamic ACKs (single write multicast or unicast) for chosen messages. 

```cpp
radio.send(&data, 32, 1); // Sends a payload with no acknowledgement requested
radio.send(&data, 32, 0); // Sends a payload using auto-retry/auto-ack features
```

_Filename: .cpp_


### function isAllowMulticast

```cpp
bool isAllowMulticast(
    void 
)
```








**Return**: If the `multicast` parameter to [write()](/Classes/classRF24/#function-write) or [send()](/Classes/classRF24/#function-send) will have any affect. This is configured using [allowMulticast()](/Classes/classRF24/#function-allowmulticast). 





















### function isPVariant

```cpp
bool isPVariant(
    void 
)
```








**Return**: `true` if the hardware is nRF24L01+ (or compatible) and `false` if it is not. 



















Determine whether the hardware is an nRF24L01+ or not. 


### function setAutoAck

```cpp
void setAutoAck(
    bool enable
)
```


**Parameters**: 

  * **enable** Whether to enable (`true`) or disable (`false`) the auto-acknowledgment feature for all pipes 


























Enable or disable the auto-acknowledgement feature for all pipes. This feature is enabled by default. 


### function setAutoAckBin

```cpp
void setAutoAckBin(
    uint8_t binary_enable
)
```


**Parameters**: 

  * **binary_enable** A binary integer to control the auto-acknowledgement feature for all pipes. Bit positions 0-5 represent pipes 0-5 respectively. A high bit (`1`) enables the feature for the corresponding pipe; a low bit (`0`) disables the feature for the corresponding pipe. 


























Enable or disable the auto-acknowledgement feature for a specific pipe. This feature is enabled by default for all pipes. 


### function setAutoAck

```cpp
void setAutoAck(
    bool enable,
    uint8_t pipe
)
```


**Parameters**: 

  * **enable** Whether to enable (`true`) or disable (`false`) the auto-acknowledgment feature for the specified pipe 
  * **pipe** Which pipe to configure. This number should be in range [0, 5]. 


























Enable or disable the auto-acknowledgement feature for a specific pipe. This feature is enabled by default for all pipes. 


### function getAutoAck

```cpp
bool getAutoAck(
    uint8_t pipe =0
)
```


**Parameters**: 

  * **pipe** The specific pipe about which data to fetch. If this parameter is not specified, then the status of the auto-ack feature about pipe 0 is returned. 







**Return**: 

* `true` if the auto-ack feature is enabled for the specified `pipe`
* `false` if the auto-ack feature is disabled for the specified `pipe`



















Fetch the status of the auto-ack feature for a specific pipe. 


### function getAutoAckBin

```cpp
uint8_t getAutoAckBin(
    void 
)
```








**Return**: A binary integer where each bit represents the auto-acknowledgement feature configuration for a specific pipe. Bit position 0 represents pipe 0, and bit position 5 represents pipe 5. A high bit (`1`) enables the feature for the corresponding pipe; a low bit (`0`) disables the feature for the corresponding pipe. Bit positions 6 and 7 will always be `0`. 



















Fetch the status of the auto-ack feature for all pipes. 


### function setPaLevel

```cpp
void setPaLevel(
    uint8_t level,
    bool lnaEnable =1
)
```


**Parameters**: 

  * **level** The desired Power Amplifier Level as defined by [rf24_pa_dbm_e](/Files/RF24Revamped_8h/#enum-rf24_pa_dbm_e). 
  * **lnaEnable** Enable or Disable the LNA (Low Noise Amplifier) Gain. See table for Si24R1 modules below. `lnaEnable` only affects nRF24L01 modules with an LNA chip. 
| `level` (enum value)   | nRF24L01   | Si24R1 with
`lnaEnabled` = 1   | Si24R1 with
`lnaEnabled` = 0    |
|  -------- | -------- | -------- | -------- |
| [RF24_PA_MIN](/Files/RF24Revamped_8h/#enumvalue-rf24_pa_min) \ (0)   | -18 dBm   | -6 dBm   | -12 dBm    |
| [RF24_PA_LOW](/Files/RF24Revamped_8h/#enumvalue-rf24_pa_low) \ (1)   | -12 dBm   | 0 dBm   | -4 dBm    |
| [RF24_PA_HIGH](/Files/RF24Revamped_8h/#enumvalue-rf24_pa_high) \ (2)   | -6 dBm   | 3 dBm   | 1 dBm    |
| [RF24_PA_MAX](/Files/RF24Revamped_8h/#enumvalue-rf24_pa_max) \ (3)   | 0 dBm   | 7 dBm   | 4 dBm    |












**Note**: 

```
The getPaLevel() function does not care what was passed `lnaEnable` parameter.
```














Set Power Amplifier (PA) level and Low Noise Amplifier (LNA) state 


### function getPaLevel

```cpp
uint8_t getPaLevel(
    void 
)
```








**Return**: One of the values defined by [rf24_pa_dbm_e](/Files/RF24Revamped_8h/#enum-rf24_pa_dbm_e). See tables in [setPaLevel()](/Classes/classRF24/#function-setpalevel)



















Fetches the current Power Amplifier Level. 


### function lastTxArc

```cpp
uint8_t lastTxArc(
    void 
)
```








**Return**: Returns values from 0 to 15. !!! hint 

```
The maximum limit of this number is controlled via the `count`
parameter to the setAutoRetry() function.
```



















Returns automatic retransmission count (ARC_CNT)

Value resets with each new transmission. Allows roughly estimating signal strength. 


### function setDataRate

```cpp
void setDataRate(
    rf24_datarate_e speed
)
```


**Parameters**: 

  * **speed** Specify one of the following values (as defined by [rf24_datarate_e](/Files/RF24Revamped_8h/#enum-rf24_datarate_e)): 
| `speed` (enum value)   | description    |
|  -------- | -------- |
| [RF24_1MBPS](/Files/RF24Revamped_8h/#enumvalue-rf24_1mbps) (0)   | for 1 Mbps    |
| [RF24_2MBPS](/Files/RF24Revamped_8h/#enumvalue-rf24_2mbps) (1)   | for 2 Mbps    |
| [RF24_250KBPS](/Files/RF24Revamped_8h/#enumvalue-rf24_250kbps) (2)   | for 250 kpbs    |



!!! warning 

```
Setting @ref RF24_250KBPS will fail for non-plus modules
(when isPVariant() returns `false`).
```







**Return**: true if the change was successful 



















Set the transmission Data Rate 


### function getDataRate

```cpp
rf24_datarate_e getDataRate(
    void 
)
```








**Return**: One of the values defined by [rf24_datarate_e](/Files/RF24Revamped_8h/#enum-rf24_datarate_e). See table in [setDataRate()](/Classes/classRF24/#function-setdatarate)



















Fetches the currently configured transmission Data Rate 


### function setCrc

```cpp
void setCrc(
    uint8_t length
)
```


**Parameters**: 

  * **length** Specify the CRC checksum length in bytes 
| `length` | description    |
|  -------- | -------- |
| 0   | to disable using CRC checksums    |
| 1   | to use 8-bit checksums    |
| 2   | to use 16-bit checksums    |












**Note**: 

```
CRC checking cannot be disabled if auto-ack is enabled.
Additionally, CRC checksum is automatically used when the auto-ack
feature is enabled.
```














Set the CRC checksum length (in bytes) 


### function getCrc

```cpp
uint8_t getCrc(
    void 
)
```








**Return**: The number of bytes used for a CRC checksum (see table in [setCrc()](/Classes/classRF24/#function-setcrc)) 





**Note**: 

```
CRC checksum is automatically used when the auto-ack feature is enabled.
```














Get the CRC checksum length (in bytes) 


### function update

```cpp
uint8_t update(
    void 
)
```








**Return**: Current value of STATUS register 



















Refresh data (from the STATUS register) used by the following functions: [irqDf()](/Classes/classRF24/#function-irqdf), irqDd(), [irqDr()](/Classes/classRF24/#function-irqdr), [isTxFull()](/Classes/classRF24/#function-istxfull), [pipe()](/Classes/classRF24/#function-pipe). 


### function irqDr

```cpp
bool irqDr(
    void 
)
```








**Return**: A bool flag that describes if the "Data Ready" event has occured. 





















### function irqDs

```cpp
bool irqDs(
    void 
)
```








**Return**: A bool flag that describes if the "Data Sent" event has occured. 





















### function irqDf

```cpp
bool irqDf(
    void 
)
```








**Return**: A bool flag that describes if the "Data Fail" event has occured. 





















### function isTxFull

```cpp
bool isTxFull(
    void 
)
```








**Return**: A bool flag that describes if all 3 levels of the TX FIFO are occupied with a payload. 





















### function pipe

```cpp
uint8_t pipe(
    void 
)
```








**Return**: The pipe number that received the next available payload in the RX FIFO is in range [0, 5]. If there is no payload in the RX FIFO, then the number returned is 255. 





















### function interruptConfig

```cpp
void interruptConfig(
    bool dataReady =true,
    bool dataSent =true,
    bool dataFail =true
)
```


**Parameters**: 

  * **dataReady** `true` ignores the "data received" event, `false` reflects the "data received" event on the IRQ pin. 
  * **dataSent** `true` ignores the "data sent" event, `false` reflects the "data sent" event on the IRQ pin. 
  * **dataFail** `true` ignores the "data failed" event, `false` reflects the "data failed" event on the IRQ pin. 


























This function is used to configure what events will trigger the Interrupt Request (IRQ) pin active LOW. The following events can be configured:

1. "data sent": This does not mean that the data transmitted was recieved, only that the attempt to send it was complete.
2. "data failed": This means the data being sent was not recieved. This event is only triggered when the auto-ack feature is enabled.
3. "data received": This means that data from a receiving payload has been loaded into the RX FIFO buffers. Remember that there are only 3 levels available in the RX FIFO buffers.
By default, all events are configured to trigger the IRQ pin active LOW. When the IRQ pin is active, use [clearStatusFlags()](/Classes/classRF24/#function-clearstatusflags) to determine what events triggered it. Remeber that calling [clearStatusFlags()](/Classes/classRF24/#function-clearstatusflags) also clears these events' status, and the IRQ pin will then be reset to inactive HIGH.

The following code configures the IRQ pin to only reflect the "data received" event: 

```cpp
radio.interruptConfig(0, 0, 1);
```

_Filename: .cpp_


### function startCarrierWave

```cpp
void startCarrierWave(
    void 
)
```



























Transmission of constant carrier wave with defined frequency and output power !!! warning 

```
If isPVariant() returns `true`, then this function takes extra
measures that alter some settings. These settings alterations include:

- setAutoAck() to `false` (for all pipes)
- setAutoRetry() to retry `0` times with a delay of 250 microseconds
- set the TX address to 5 bytes of `0xFF`
- flushTx()
- load a 32 byte payload of `0xFF` into the TX FIFO's top level
- setCrc() to `0` (disabling CRC checking).
```


### function stopCarrierWave

```cpp
void stopCarrierWave(
    void 
)
```







**See**: [startCarrierWave()](/Classes/classRF24/#function-startcarrierwave)




















Stop transmission of constant wave and reset PLL and CONT registers !!! warning 

```
This function will powerDown() the radio per recommendation
of datasheet.
```

 !!! important 

```
If isPVariant() returns `true`, please remember to
re-configure the radio's settings

```cpp
// re-establish default settings
setCrc(RF24_CRC_16);
setAutoAck(true);
setAutoRetry(5, 15);
```
```


### function openReadingPipe

```cpp
void openReadingPipe(
    uint8_t number,
    uint64_t address
)
```


**Parameters**: 

  * **number** Which pipe number to open, should be in range [0, 5]. 
  * **address** The 40-bit address of the pipe to open. 






**See**: [openReadingPipe(uint8_t, const uint8_t*)](/Classes/classRF24/#function-openreadingpipe) !!! important 

```
Pipes 1-5 should share the first 32 bits.
Only the least significant byte should be unique, e.g.
```cpp
    openReadingPipe(1, 0xF0F0F0F0AA);
    openReadingPipe(2, 0xF0F0F0F066);
```
```

 !!! warning 

```
Pipe 0 is also used by the writing pipe so should typically be
avoided as a reading pipe.

If used, the reading pipe 0 address needs to be restored at avery call to
startListening(), and the address is ONLY restored if the LSB is a
non-zero value.

Read [this article](http://maniacalbits.blogspot.com/2013/04/rf24-addressing-nrf24l01-radios-require.html) to understand how to avoid
using malformed addresses.
```




















Open a pipe for reading 


### function openWritingPipe

```cpp
void openWritingPipe(
    uint64_t address
)
```


**Parameters**: 

  * **address** The 40-bit address of the pipe to open. 






**See**: openWritingPipe(const uint8_t)




















Open a pipe for writing 
Addresses are 40-bit hex values, e.g.:



```cpp
openWritingPipe(0xF0F0F0F0F0);
```

_Filename: .cpp_


### function ce

```cpp
void ce(
    bool level
)
```


**Parameters**: 

  * **level** Use `true` for active `HIGH` state. Use `false` for inactive `LOW` state. !!! important 

```
Please see data sheet for a much more detailed description of this
pin's usage.
```


























Set the radio's CE (Chip Enable) pin. In RX mode, this pin controls weather the radio is actively listening. In TX mode, this pin controls how much data from the TX FIFO buffers is transmitted. Keep in mind that a minimum 10 microseconds pulse will send only 1 payload from the TX FIFO, and the radio requires at least a 130 microsecond pulse to start actively listening in RX mode. 



## Protected Functions Documentation

### function beginTransaction

```cpp
inline void beginTransaction()
```



























For storing the result of testing the toggleFeatures() affect [SPI](/Classes/classSPI/) function to begin transactions that includes setting CSN pin active LOW 


### function endTransaction

```cpp
inline void endTransaction()
```



























[SPI](/Classes/classSPI/) function to end transactions that includes setting CSN pin inactive HIGH 


### function csn

```cpp
void csn(
    bool mode
)
```


**Parameters**: 

  * **mode** HIGH to take this unit off the [SPI](/Classes/classSPI/) bus, LOW to put it on 


























Set chip select pin

Running [SPI](/Classes/classSPI/) bus at PI_CLOCK_DIV2 so we don't waste time transferring data and best of all, we make use of the radio's FIFO buffers. A lower speed means we're less likely to effectively leverage our FIFOs and pay a higher AVR runtime cost as toll. 


### function read_register

```cpp
void read_register(
    uint8_t reg,
    uint8_t * buf,
    uint8_t len
)
```


**Parameters**: 

  * **reg** Which register. Use constants from [nRF24L01.h](/Files/nRF24L01_8h/#file-nrf24l01.h)
  * **buf** Where to put the data 
  * **len** How many bytes of data to transfer 







**Return**: Nothing. Older versions of this function returned the status byte, but that it now saved to a private member on all [SPI](/Classes/classSPI/) transactions. 



















Read a chunk of data in from a register 


### function read_register

```cpp
uint8_t read_register(
    uint8_t reg
)
```


**Parameters**: 

  * **reg** Which register. Use constants from [nRF24L01.h](/Files/nRF24L01_8h/#file-nrf24l01.h)







**Return**: Current value of register `reg`



















Read single byte from a register 


### function write_register

```cpp
void write_register(
    uint8_t reg,
    const uint8_t * buf,
    uint8_t len
)
```


**Parameters**: 

  * **reg** Which register. Use constants from [nRF24L01.h](/Files/nRF24L01_8h/#file-nrf24l01.h)
  * **buf** Where to get the data 
  * **len** How many bytes of data to transfer 







**Return**: Nothing. Older versions of this function returned the status byte, but that it now saved to a private member on all [SPI](/Classes/classSPI/) transactions. 



















Write a chunk of data to a register 


### function write_register

```cpp
void write_register(
    uint8_t reg,
    uint8_t value,
    bool is_cmd_only =false
)
```


**Parameters**: 

  * **reg** Which register. Use constants from [nRF24L01.h](/Files/nRF24L01_8h/#file-nrf24l01.h)
  * **value** The new value to write 
  * **is_cmd_only** If this is true then only the `reg` parameter is written like a [SPI](/Classes/classSPI/) cmd ( `value` parameter is ignored) 







**Return**: Nothing. Older versions of this function returned the status byte, but that it now saved to a private member on all [SPI](/Classes/classSPI/) transactions. 



















Write a single byte to a register 





## Public Attributes Documentation

### variable txDelay

```cpp
uint32_t txDelay;
```



























The driver will delay for this duration when [stopListening()](/Classes/classRF24/#function-stoplistening) is called

When responding to payloads, faster devices like ARM(RPi) are much faster than Arduino:

1. Arduino sends data to RPi, switches to RX mode
2. The RPi receives the data, switches to TX mode and sends before the Arduino radio is in RX mode
3. If AutoACK is disabled, this can be set as low as 0. If AA/ESB enabled, set to 100uS minimum on RPi !!! warning 

```
If set to 0, ensure 130uS delay after stopListening() and
before any calls to send()
```


### variable csDelay

```cpp
uint32_t csDelay;
```



























On all devices but Linux and ATTiny, a small delay is added to the CSN toggling function

This is intended to minimise the speed of [SPI](/Classes/classSPI/) polling due to radio commands

If using interrupts or timed requests, this can be set to 0 Default:5 






-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time