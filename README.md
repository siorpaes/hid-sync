# hid-sync
HID keyboard with synced external actuation.
The purpose of this project is to solve the problem of visual art performers who need to synchronize a video clip with some external actuations such as lamps, pumps, motors, whatever can be managed by a relay.
The firmware acts as a normal USB HID keyboard: when pressing the button, a defined key (tyipically space-bar) is sent to the connected device (PC, tablet, smartphone) so to start the video clip. A timer synchronizes with the button press so that an external supply can be turned on or off after a defined interval. 
In this way, it is possible to synchronize the driving of external loads with whatever video clip.

## Bill of material
* [Nucleo-F042K6 board](https://www.st.com/en/evaluation-tools/nucleo-f042k6.html)
* [Relay board](https://www.amazon.it/gp/product/B06XHJ2PBJ/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&psc=1)
* [Buttons](https://www.amazon.it/gp/product/B07XQSBW7Q/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&psc=1)
* [LED holders](https://www.amazon.it/gp/product/B01MRVAFGK/ref=ppx_yo_dt_b_asin_title_o01_s01?ie=UTF8&psc=1)
* USB cable 


The project targets a Nucleo-F042K6 board from STMicroelectronics but can be easiy adapted to any STM32 with USB device capabilities.

## Pinout

|Signal           | STM32 IO |  Nucleo connector  |
|-----------------|:--------:|:------------------:|
| Button          |   PB5    |    CN3-14 [D11]    |
| LED             |   PB1    |    CN3-9  [D6]     |
| Relay           |   PB7    |    CN3-7  [D4]     |
| Spare OUT       |   PB6    |    CN3-8  [D5]     |
| Spare IN        |   PB4    |    CN3-15 [D12]    |
| USB DP (Green)  |   PA12   |    CN3-5  [D2]     |
| USB DM (White)  |   PA11   |    CN3-13 [D10]    |
