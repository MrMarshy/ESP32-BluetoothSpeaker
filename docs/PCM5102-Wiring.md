# PCM5102 Wiring

Wiring Pinout:

DAC BOARD   > Raspberry Pi 3 Model B connector J8
-----------------------------------------------
SCK         > Not wired (Internally generated)
BCK         > PIN 12    (GPIO18)
DIN         > PIN 40    (GPIO21)
LRCK        > PIN 35    (GPIO19)
GND         > PIN 6     (GND) Ground
VIN         > PIN 2     (5V)

FLT             > GND 
DEMP            > GND 
XSMT            > I Left it floating and it worked, should be tied high to unmute and grounded to mute.
FMT             > GND 