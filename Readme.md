Custom Bootloader for 3DoT Board
================

**Installing in Arduino IDE**
1. In the Arduino IDE, Navigate to File->Preferences and paste
   https://github.com/Jaapdedood/3DoTBootloader/raw/master/package_3DoT_index.json
   into "Additional Board Manager URLs"
2. Open Tools->Board->Board Manager and Search "3DoT"
3. Install the 3DoT board

**Building in Atmel Studio**

1. Complete the above steps, "Installing in Arduino IDE" 
2. In Atmel Studio, create a new project from arduino sketch
3. Select the "Arxterra 3DoT" as target board
4. Build your project.

**Building from source**

1. Navigate to bootloaders/caterina/
2. Type 'make'.

Version History
===============
```
v1.0.0
* Bootloader fully working as intended: Stay in bootloader as long as switch is
in "BOOT" position.
* Entering bootloader requires device to transition OFF -> BOOT. ON -> BOOT does
not work. BOOT -> ON works i.e. loads sketch.
* Code now based on Polulu A-Star 32U4 Micro bootloader for better compatability

v0.3-Beta Release (8/18/18)
* Board files fully functioning with Arduino IDE and Atmel Studio
* Unable to stay in bootloader.
```
