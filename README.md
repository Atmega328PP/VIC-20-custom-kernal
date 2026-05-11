# VIC-20-custom-kernal

The primary focus of this project is to enable the C16 keyboard to control the VIC-20 identically to the standard VIC-20 keyboard. Both boards are pin compatible but their matrices are different, the custom kernal aims to fix this by swapping the PETSCII codes in the keyboard scanning array.

Curtesy to Lee Davison for the incredible complete BASIC+Kernal dissasembly, this project would be significantly more difficult without it. 

# Building

This is a little bit odd, the dissasembly that it's based off of will only assemble via Kowalski's 6502 Simulator assembler, it's a quality program that is currently required to build the ROM. The disassembly currently contains both the BASIC interpreter and the Kernal, these are on seperate chips physically so this requires them to be seperated before flashing. My current solution is to just assemble the entire file and then split the binary at $C004 with a hex editor. I am working on splitting the assembly to where it doesn't include the BASIC interpreter but currently it will assemble and function via this method.








This project is WIP, not everything works properly yet but it is being worked on continuously.
TODO/Not currently functional:

CTRL table
Commodore table is a little bit questionable
Remove BASIC interpreter from Kernal disassembly
