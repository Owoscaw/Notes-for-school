

An instruction set describes the set of commands that a processor can perform. Different types of processors (AMD, Intel) can have different instruction sets however execute similar commands. This set of instructions are hard coded onto a processor, they are physical circuits.

An instruction may perform different types of instructions: Data transfer, Arithmetic, Comparison, Logical (AND NOT OR), Branch, Shift (shifting bits left or right).

Machine code is the binary version of the instruction set, the only code that the processor can directly understand. It is the lowest level code and depends on the word length of the processor. An instruction consists of the Operation code and the Operand. The Operation code (opcode) is the actual command or specifies whether the operand is a memory address of a data value. The operand is one or many items of data. The opcode defines if the operand is a value or memory address (including registers). 

For example the first 8 bits of an instruction could be dedicated for the opcode, the first 6 representing the actual command and the latter 2 representing the addressing mode (if the operand is an address, register, or value). The last 8 bits could represent the operand. The addressing mode typically takes up 2 bits and describes the operand.

Immediate addressing is where the operand is an actual value to be used in an instruction. This is represented by the addressing mode 00. Direct addressing is where the operand is an address to be used in an instruction. This is represented by the addressing mode 01.








