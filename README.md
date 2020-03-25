# Rock64-R64.GPIO
A Python GPIO library for the Rock64 single-board computer ([RPi.GPIO](https://sourceforge.net/projects/raspberry-gpio-python/) clone).

## Python Libraries and Scripts

**R64.GPIO**<br>
A re-implementation of the RPi.GPIO library for the Rock64. Currently under development.<br>

I found that on kernel version 4.4.124 the pin channels are offset by 1000, so I added a function ("offset") to check the kernel version and add the offset accordingly. Please use the 'Armbian-Xenial-kernel-4.4.103-to-4.4.156' branch if you are still using those particula kernel versions.


See [the wiki](https://github.com/Leapo/Rock64-R64.GPIO/wiki) for documentation on [Functions](https://github.com/Leapo/Rock64-R64.GPIO/wiki/Functions) and [GPIO Modes](https://github.com/Leapo/Rock64-R64.GPIO/wiki/GPIO-Modes).

**R64-GPIO-test.py**<br>
A simple test script. Outputs a list of internal vars, sets the GPIO mode to "BOARD", sets up a GPIO output (blinks an LED if connected to pin 16), sets up a GPIO input (pulls-up and reports the state of pin 18), then cleans up all GPIO exports and exits.

## Library Installation and Usage:
**Importing R64.GPIO**<br>
Below is the reccomended method for importing this library into your project. For alternate methods, see the [Installation and Usage](https://github.com/Leapo/Rock64-R64.GPIO/wiki/Installation-and-Usage) page in the wiki.
1. Download the entire "R64" folder from the repo.
1. Place the "R64" folder in the same directory as the Python script you're working with.
1. Within your script, substitute the traditional "`import RPi.GPIO as GPIO`" line for "`import R64.GPIO as GPIO`".

Once imported, syntax for implemented functions should be identical to RPi.GPIO.

# Test Platform

All testing of this library is done on a Rock64 (4GB model) running [Armbian_5.42_Rock64](https://dl.armbian.com/rock64/Ubuntu_xenial_default.7z) (Ubuntu Xenial).

Compatability with other versions of Linux running on the Rock64 is not gauranteed.

# Resources
List of resources and reference material used while building the scripts and libraries in this repository
* [Github- Leapo](https://github.com/Leapo/Rock64-R64.GPIO)
* [Pine64 Forum - GPIO LED blinker using SYSFS on the Rock64](https://forum.pine64.org/showthread.php?tid=4695)
