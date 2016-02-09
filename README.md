# Wintron

Firmware for the Trekstor Wintron 7 Touch.
Needs to be placed in /lib/firmware.

Driver: https://github.com/onitake/gslx680-acpi

For some reason even after calibrating the touchscreen there was a mapping problem with the x axis.
We fixed that by adding
```
x = (int) (x*114) / 100;
```
in line 351 of the Silead GSLx680 driver source.
