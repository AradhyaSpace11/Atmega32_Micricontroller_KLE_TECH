Table of Contents
ADD - Add without Carry
ADC - Add with Carry
SUB - Subtract without Carry
SBC - Subtract with Carry
ADIW - Add Immediate to Word
SBIW - Subtract Immediate from Word
MUL - Multiply Unsigned
INC - Increment
DEC - Decrement
ADD - Add without Carry
Description: Adds the contents of register Rr to register Rd and places the result in register Rd.

Syntax: ADD Rd, Rr

Example:

asm
Copy code
; Add contents of R1 to R0
ADD R0, R1
Common Mistakes:

Forgetting that the result is stored in Rd, not Rr.
Not considering that this operation affects the Zero (Z) and Carry (C) flags.
ADC - Add with Carry
Description: Adds the contents of register Rr and the Carry flag to register Rd.

Syntax: ADC Rd, Rr

Example:

asm
Copy code
; Add contents of R1 and Carry flag to R0
ADC R0, R1
Common Mistakes:

Overlooking the Carry flag's initial value. Ensure it's correctly set or cleared before this operation depending on your requirements.
SUB - Subtract without Carry
Description: Subtracts the contents of register Rr from register Rd.

Syntax: SUB Rd, Rr

Example:

asm
Copy code
; Subtract R1 from R0
SUB R0, R1
Common Mistakes:

Ignoring flag effects, such as the Negative (N) flag, which can impact subsequent conditional operations.
SBC - Subtract with Carry
Description: Subtracts the contents of register Rr and the Carry flag from register Rd.

Syntax: SBC Rd, Rr

Example:

asm
Copy code
; Subtract R1 and Carry flag from R0
SBC R0, R1
Common Mistakes:

Not properly managing the Carry flag before execution, which can lead to unexpected results.
ADIW - Add Immediate to Word
Description: Adds an immediate value (K) to a word in the register pair.

Syntax: ADIW Rd, K

Example:

asm
Copy code
; Add immediate value 3 to register pair R24:R25
ADIW R24, 3
Common Mistakes:

Using a register pair that's not R24-R31 (even).
Forgetting the immediate value range is 0-63.
SBIW - Subtract Immediate from Word
Description: Subtracts an immediate value (K) from a word in the register pair.

Syntax: SBIW Rd, K

Example:

asm
Copy code
; Subtract immediate value 2 from register pair R26:R27
SBIW R26, 2
Common Mistakes:

Similar to ADIW, using an incorrect register pair or an out-of-range immediate value.
MUL - Multiply Unsigned
Description: Multiplies the contents of registers Rd and Rr.

Syntax: MUL Rd, Rr

Example:

asm
Copy code
; Multiply R0 by R1
MUL R0, R1
Common Mistakes:

Not remembering the result is stored in R0:R1, affecting these registers' previous values.
INC - Increment
Description: Increments the content of register Rd by 1.

Syntax: INC Rd

Example:

asm
Copy code
; Increment R0
INC R0
Common Mistakes:

Assuming this instruction does not affect the Zero (Z) flag when the result is 0xFF + 1.
DEC - Decrement
Description: Decrements the content of register Rd by 1.

Syntax: DEC Rd

Example:

asm
Copy code
; Decrement R0
DEC R0
Common Mistakes:

Forgetting that like INC, DEC also affects the Zero (Z) flag if the result is 0x00 - 1.
