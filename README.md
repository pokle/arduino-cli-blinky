# Checkout out the Arduino cli

Install from https://github.com/arduino/arduino-cli

# Commands

```
$ arduino-cli core install arduino:avr

$ arduino-cli board list | grep -i ard
Port                            Type              Board Name          FQBN           
/dev/cu.usbmodem14401           Serial Port (USB) Arduino/Genuino Uno arduino:avr:uno

$ set FQBN arduino:avr:uno
$ arduino-cli compile --fqbn $FQBN
Build options changed, rebuilding all
Sketch uses 930 bytes (2%) of program storage space. Maximum is 32256 bytes.
Global variables use 9 bytes (0%) of dynamic memory, leaving 2039 bytes for local variables. Maximum is 2048 bytes.

$ ls -l
total 56
-rwxr-xr-x  1 tushar  staff  14020 Aug  4 10:42 MyFirstSketch.arduino.avr.uno.elf
-rw-r--r--  1 tushar  staff   2640 Aug  4 10:42 MyFirstSketch.arduino.avr.uno.hex
-rw-r--r--  1 tushar  staff    166 Aug  4 10:21 MyFirstSketch.ino
-rw-r--r--  1 tushar  staff    413 Aug  4 10:41 README.md

$ set PORT /dev/cu.usbmodem14401
$ arduino-cli upload -p $PORT --fqbn $FQBN
```
