Custom Bootloader for 3DoT Board
================
**Updated install instructions:**
https://www.arxterra.com/getting-started-with-3dot-initial-arduino-setup/

**Installing in Arduino IDE (from github)(not recommended)**
1. In the Arduino IDE, Navigate to File->Preferences and paste
   https://github.com/Jaapdedood/3DoTBootloader/raw/master/package_3DoT_index.json
   into "Additional Board Manager URLs".
2. Open Tools->Board->Board Manager and Search "3DoT".
3. Install the 3DoT board.

**Building in Atmel Studio (not tested)**

1. Complete the above steps, "Installing in Arduino IDE" .
2. In Atmel Studio, create a new project from arduino sketch.
3. Select the "Arxterra 3DoT" as target board.
4. Build your project.

**Building from source**

1. Navigate to bootloaders/caterina/
2. Type 'make'.

Version History
===============
```
v2.1.0 (07/11/19)
* SetupCurrentLimit and accompanying TWI functions added to set MCP4017
resistance via I2C before starting a sketch.
* Bug: need to wait a few seconds before being able to upload a sketch with
switch in "program" position (bug always existed).

v2.0.0 (11/14/18)
* Code overhaul. v1.0.0 was not working on v7 3DoT board. Continuously doing a
board reset would cause the USB interface to continuously disconnect from the host.
* Now stays within a single while loop while switch is in BOOT position, rather
than resetting the board.
* All checks and references to SREG flags removed.
* All references to watchdog removed.

v1.0.0 (08/20/18)
* Bootloader working as intended: Stay in bootloader as long as switch is
in "BOOT" position.
* Entering bootloader requires device to transition OFF -> BOOT. ON -> BOOT does
not work. BOOT -> ON works i.e. loads sketch.
* Code now based on Polulu A-Star 32U4 Micro bootloader for better compatability.

v0.3-Beta Release (08/18/18)
* Board files fully functioning with Arduino IDE and Atmel Studio.
* Unable to stay in bootloader.
```
