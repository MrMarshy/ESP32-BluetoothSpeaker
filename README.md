# ESP-IDF A2DP-SINK demo
------------------------------------------------------------------------

### Hardware Required

To play the sound, there is a need of loudspeaker and an external I2S codec. 

For the I2S codec, pick whatever chip or board works for you; this code was written using a PCM5102 chip, but other I2S boards and chips will probably work as well. The default I2S connections are shown below, but these can be changed in menuconfig:

| ESP pin   | I2S signal   | Comment |
| :-------- | :----------- |:------- |
| GPIO22    | LRCK         |         |
| GPIO25    | DATA         |         |
| GPIO26    | BCK          |         |
| Not Wired | SCK          | Internally Generated|
| 5V        | VIN          |        |
| GND       | FLT           |       |
| GND       | DEMP          |       |
| 5V        | XSMT          | High to unmute, GND to mute|
| GND       | FMT           |       |



### Configure the project

```
idf.py menuconfig
```

* Set the use of external I2S codec or internal DAC for audio output, and configure the output PINs under A2DP Example Configuration

* Enable Classic Bluetooth and A2DP under Component config --> Bluetooth --> Bluedroid Enable

### Build and Flash

Build the project and flash it to the board, then run monitor tool to view serial output.

```
idf.py -p PORT flash monitor
```

(To exit the serial monitor, type ``Ctrl-]``.)
