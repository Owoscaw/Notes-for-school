

Similar to the human brain, a processor controls, calculates, and executes instructions. A processor has different components: Arithmetic Logic Unit (ALU), control unit, clock, general purpose registers, dedicated register. Each part of the processor is a very complex [[Circuits|circuit]].

The Arithmetic Logic Unit is responsible for problem-solving within the processor. It performs arithmetic, logical and shift operations on data. The result of two inputs going through the ALU is stored in the accumulator.

The control unit coordinates the activity of other components. It is regulated by the clock. Each instruction is accepted and decoded, separate steps such as fetching the address of a data and fetching data itself are separated.

The system clock is a component that regularly sends on and off signals that synchronise operations inside the processor. Instructions are performed on the rising edge of a pulse. Actions take a fixed number of cycles to complete

## Registers:

General purpose registers store the results of the ALU so that it is not lost. Rather than writing the results of the ALU directly to memory, which can take a long time relative to the processor, it is stored in a general purpose register temporarily until it is needed. The accumulator is an example of a general purpose register.

Dedicated registers are the same as general purpose registers in the sense that they are susuperfastemory units used by the processor, however they have a dedicated purpose: the Program Counter holds memory locations of the next instruction to be executed. Current Instruction Register holds the current instruction. The Memory Address Register holds the address in memory where the processor is required to fetch or store data from or to. Memory Buffer Register temporarily holds data moving between the processor and main memory. The statusatus register holds information about the current state of operations. It is used to set flags or detect error conditions.

The fetch execute cycle is the process that is repeated for every instruction that makes up a program, regulated by the system clock.


## Fetch:
In the fetch part of the cycle, the address of the next instruction is fetched from the program counter, which is then incremented by one. The address is transferred to the memory address register  where it is then sent along the address bus to main memory along with a control signal where the next instruction is sent from main memory to the memory buffer register. After the next instruction has been received, it is transferred to the current instruction register.

## Decode:
Now that the instruction is in the current instruction register, it is decoded. The action that now needs to be carried out is determined by the contents of the instruction compared to the [[Processor instruction set]]. If additional data is required to complete the decoded instruction, the memory address register and memory buffer register are used to load this data into the ALU and associated registers.

## Execute:
All the information needed to execute the instruction is now in the ALU and general purpose registers connected to the ALU. Results produced from the ALU are stored in nearby registers, the accumulator, or it is written to memory depending on the instructions received.
