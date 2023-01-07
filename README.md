# I2SClocklessLedDriver for esp32s3
## Introduction
### What kind of led do you want to drive
This library is a new take on driving ws2812 leds with I2S on an esp32. It allows to drive up to 16 strips leds in parallel of  
* RGB:
    * WS2812,
    * WS2813,
    * WS2815 
* RGBW 
    * SK6812. 

this is the first version not all the functionalities of the I2SClocklessledDriver for esp32 are present yet. If I there is enough interest then I will do.

### What is to know
* The LCD driver for the esp32S3 doesn't work as the same as the lcd for the esp32. Hence the implementation is different. It is required to transform all the leds into a big buffer.
* You need to activate the PSRAM for it to work as the buffers are declared in PSRAM
* Do  not hesitate to contact me 

