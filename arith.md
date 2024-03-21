# ATmega32 Arithmetic Instructions Guide

This guide aims to provide clear examples, explanations, and common mistakes for each arithmetic instruction available on the ATmega32 microcontroller.

## ADD - Add without Carry

### Description
The `ADD` instruction adds the contents of two registers without the carry and stores the result in the destination register. It's a fundamental arithmetic operation used in numerous algorithms and routines.

### Syntax
```assembly
; Adds the content of R2 to R1 and stores the result in R1
ADD R1, R2
'''
