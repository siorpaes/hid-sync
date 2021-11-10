# hid-sync
HID keyboard with synced external actuation.
The purpose of this project is to solve the problem of visual art performers who need to synchronize a video clip with some external actuations such as lamps, pumps, motors, whatever can be managed by a relay.
The firmware acts as a normal USB HID keyboard: when pressing the button, a defined key (tyipically space-bar) is sent to the connected device (PC, tablet, smartphone) so to start the video clip. A timer synchronizes with the button press so that an external supply can be turned on or off after a defined interval. 

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
