---
title: Common Issues


---

# Common Issues



# Settings that must match

Before you report undesirable behavior, please make sure that the following [RF24](/Classes/classRF24/) configurations match on both receiving and transmitting nRF24L01 transceivers:



1. [RF24::setAddressLength()](/Classes/classRF24/#function-setaddresslength)
2. [RF24::setChannel()](/Classes/classRF24/#function-setchannel)
3. [RF24::setDataRate()](/Classes/classRF24/#function-setdatarate)
4. [RF24::setAutoAck()](/Classes/classRF24/#function-setautoack)
5. [RF24::setDynamicPayloads()](/Classes/classRF24/#function-setdynamicpayloads) or RF24::disableDynamicPayloads()
6. [RF24::enableAckPayload()](/Classes/classRF24/#function-enableackpayload) or [RF24::disableAckPayload()](/Classes/classRF24/#function-disableackpayload) (requires auto-ack and dynamic payloads features)
7. [RF24::setPayloadLength()](/Classes/classRF24/#function-setpayloadlength) (only if the dynamic payloads feature is disabled &ndash; it is disabled by default)
8. [RF24::setCrc()](/Classes/classRF24/#function-setcrc) (the auto-ack feature automatically enables CRC because it is required)
Also, it helps to think of an address as a path (a commonly shared route) instead of an identifying device destination. This means that addresses have to match for a payload to travel from one transceiver to another. However, the pipe numbers assigned with the matching address do not have to match. You can think of pipes as parking spots for the packets, while all packets' payloads live in a TX or RX FIFO buffer. Remember that the TX FIFO buffers and the RX FIFO buffers both have a maximum occupancy of 3 payloads (regardless of the maximum 32-byte payload size). 


# The most common issues and their solutions


## send() always returns true after setAutoAck(false)

Don't disabled the auto-ack feature. [RF24::send()](/Classes/classRF24/#function-send) has no reason to doubt that the payload was delivered if the auto-ack feature is disabled. We recommend you read the docs about [RF24::setAutoAck()](/Classes/classRF24/#function-setautoack) before disabling the auto-ack feature. 


## send() returns false when the payload was received

If the settings match on both endpoint transceivers, then this can only mean that the receiving nRF24L01 failed to send an acknowledgement (ACK) packet back to the transmitting nRF24L01. Usually this is due to instability (electric noise) in the power lines (VCC and GND) going to the receiving nRF24L01.

If you're not receiving ACK packets correctly/reliably on data rates lower than 2MBPS, try adding a big capacitor close to the module/chip. Example issues: [#264](https://github.com/nRF24/RF24/issues/264)[#211](https://github.com/nRF24/RF24/issues/211).

For reliability, please use Electrolytic or Tantalum capacitors. Ceramic capacitors may not be good enough (depending on the manufacturing source). 

-------------------------------

Updated on 29 December 2020 at 19:03:46 Pacific Standard Time
