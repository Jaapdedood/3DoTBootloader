Lily3D bootloader for the 3DoT board in Arduino IDE 
================

**Building in Arduino IDE (prerequisite to building via Atmel Studio 7)**
1. In the Arduino IDE, Navigate to File->Preferences and paste
   https://github.com/Jaapdedood/3DoTBootloader/raw/master/package_3DoT_index.json
   into "Additional Board Manager URLs"
2. Open Tools->Board->Board Manager and Search "3DoT"
3. Install the 3DoT board

**Building in Atmel Studio**

1. Create a new project from arduino sketch
2. Select the "Arxterra 3DoT" as target board
3. Build your project.

**Building from source**

1. Navigate to cores/Lily3D/
2. Type 'make'.

Version History
===============
```
v0.3-Beta Release (8/18/18)
* Board files fully functioning with Arduino IDE and Atmel Studio
* Bootloader behavior needs to be verified with fully functioning 3DoT Board
```
