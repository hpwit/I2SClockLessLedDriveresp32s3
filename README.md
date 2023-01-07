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
* It's been tested with arduino esp32 2.0.5 core
* The LCD driver for the esp32S3 doesn't work as the same as the lcd for the esp32. Hence the implementation is different. It is required to transform all the leds into a big buffer.
* do not use pin 0. It's used in the code as 'ghost pin'. If I undo the esp_lcd_new_i80_bus, I can avoid this but i cannot ensure compatibility with the next core library ( that is what happen with the first version under esp-idf which was not compatible with v5 anymore)
* You need to activate the PSRAM for it to work as the buffers are declared in PSRAM
* Do  not hesitate to contact me 

