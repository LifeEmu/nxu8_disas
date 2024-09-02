# nxu8_disas
An nX-U8/100 disassembler written in C.

## Changes made on top of frsr's code
- Fixed some instructions
- Adjusted instruction syntaxes based on personal preferences
	- Tabs are used for spacing instead of spaces
	- Immediates does not have `#` as prefixes
	- `Dbitadr` and `Rn.bitoffset` are rewritten as `bit, [address]` and `bit, Rn`
	- Indirect addressing modes have brackets now, for example: `st r0, 0:[811Dh]`
	- The colons in `b/bl Dadr` are removed, for example `bl 03130h`
	- `lea Dadr` has brackets now: `lea [FFFCh]`

## Known bugs
- ~~`#imm7` does not show sign properly (`add er0, F0h` actually adds `FFF0h`(`-10h`) to `ER0`)~~
- `extbw` shows the register twice (`extbw er0, er0`)

## Copying
Ask frsr, I didn't do anything :p
