
Assembly code uses mnemonics to represent machine code. It is unique to a given computer architecture, similar to machine code. Assembly language translates directly into machine code, determined by a CPU's [[Processor instruction set]]. Example:

LDR R1, 300: load contents of address 300 into register 1
LDR R4, 301: load contents of address 301 into register 4
ADD R1, R1, R4: Store the addition of register 1 and register 4 in register 1
MOV R2, R1: copy contents of register 1 into register 2
SUB R3, R2, #5: subtract 5 from the value in register 2 and store it in register 3
STR R3, 302: store the contents of register 3 in memory address 302

LDR R1, 301
LDR R2, 302
LDR R3, 303
ADD R1, R1, R2
ADD R1, R1, R3
STR R1 304
HLT


Branch instructions are like if statements in python. The CMP (compare) and B (branch) commands are used. CMP, Rn, <operand> is used to compare the value in Rn to the operand. B <label> will branch the program to position <label> in the program. B <condition> <label> branches to <label> if <condition> is true. The EQ suffix means equal to 0, NE means not equal to, GT means greater than, and LT means less than. Example:


LDR R1, 301
CMP R1, 302
BGT 6
STR R1, 303
HLT
LDR R1, 302
STR 303
HLT

While loops are written using branch and compare commands. Example:

MOV R1, #0
LABEL 1
INPUT R2
ADD R1, R1, R2
CMP R2, #0
BNE LABEL 1
STR R1, 100


The logical commands for assembly code are:

\> AND Rd, Rn, <operand>: performs an AND bitwise comparison with the value in Rn and the value specified in the operand and stores the result in Rd.

\> ORR Rd, Rn, <operand>: performs an OR bitwise comparison with the value in Rn and the value specified in the operand and stores the result in Rd.

\> EOR Rd, Rn, <operand>: performs an XOR bitwise comparison with the value in Rn and the value specified in the operand and stores the result in Rd.

\> MVN Rd, <operand>: performs a bitwise NOT comparison on the value specified in the operand and stores the result in Rd.

The AND function can convert an ascii value into a pure binary value by changing the first four bits to a 0, while retaining any information in the last four bits. This would look like AND R1, R2, #00001111B. The last parameter is a binary value, specified by the "B" at the end. The OR function can be used to set certain bits to a 1 without affecting any other bits, for example: OR R1, R2, #00001111B to set the last four bits of a binary value to 1. The NOT function can be used to convert a binary number into the negative version of said number through two's compliment, as seen here: NOT R1, R1; ADD R1, R1, #1B. This would convert the binary value in register 1 to its two's compliment.

Logical shifts can also be written In assembly language using LSL and LSR, representing a logical shift left and logical shift right respectively.  For example: LSL R2, R1, #2 will shift the binary value in R1 2 bits to the left and store the result in R2. After an LSR, and there is a bit that falls off of the end, this bit is stored in the carry bit.

This fine control over bits and memory locations makes assembly language a good choice when coding drivers.






