
The definition of a computer system is a device that can take a set of inputs and process them into outputs. There has to be a stage of processing.

The central processing unit (CPU) contains many components: processor, main memory, address control and data busses, and I/O controllers. The processor is responsible for the fetch, decode, execute cycle. This cycle can be seen in more detail [[CPU and fetch-execute cycle|here]]. Busses are parralel lines along which data flows, they link different components.

I/O, Input/Output, controllers are responsible to act as an interface between a device and the processor as peripherals cannot directly connect to the processor. These connect [[Input-Output devices]] to the internal components of the computer. A device driver is a piece of software that enables interaction between a device and the I/O controller inside the CPU. The I/O controller converts signals from peripherals into signals that can be processed, and vice versa. It receives I/O requests from the CPU and sends these specific control requests to the device to be controlled. It is also responsible for managing data flow to and from the CPU and devices.

The control bus is used to send control signals between I/O controllers and the processor, as well as between the processor and memory. The data bus sends data between the CPU and components. Address bus sends memory addresses from the processor to other CPU components. System busses classify all three separate busses.

Control signals are signals that are sent in order to tell a component or device to execute a certain task. These tasks can include: memory read, memory write, bus request, bus grant, and the clock. Bus request and bus grant are control signals that indicate whether a device has permission to use the data bus.

A bus is essentially a series of wires that transfer data between internal components. They typically consist of powers of 2 lines, as they are used in parallel communication, one signal takes up multiple lines, so it is received faster.

Memory is divided into equal units called words, usually powers of 2 bits long. Each word has a separate memory address. The size of a word determines the size of the data bus and vice versa. One word can be sent at a time down the data bus.

The data bus is a bidirectionalbus, data can be sent both ways. If the width (amount of lanes) of the data bus is the same as the length of a word, an entire word can be sent along the bus in a signal operation in parallel. Bus width affects performance, as there will be a bottleneck if the data bus is not wide enough to transfer signals fast enough.

The address bus is the bus that carries the address of a memory location along one direction, from the processor to either an I/O controller or memory. This address could hold data referred to in an instruction or the next instruction itself. The width of this bus also affects performance for the same reason.

Main memory stores data and instructions that are to be processed. The number of memory addresses is constrained by the width of the address bus. Each address can store a fixed number of bits determined by the type of processor. The smallest addressable unit is called a word. Data is stored in a more permanent form in [[Storage Devices]].

The processor can request the data in a memory address by sending the "read" instruction down the control bus as well as the address along the address bus to the memory. The data will be returned to the processor along the data bus.

Early computers performed calculations based on fixed instructions that do not changed. A general purpose computer can perform different tasks at different times, with no fixed programming. According to stored program concept, machine code instructions are loaded into memory to be executed sequentially by the processor in the fetch execute cycle.

In von Neumann architecture, both the program and data are stored in memory and share a single bus between the two. Harvard architecture is an alternate model where instructions and data are in separate memories and therefore using separate busses. Both the program and the data have their own dedicated bus. This also allows for program instructions and data to be stored in unequal quantities as well as unequal word lengths and bus widths.

The Harvard architecture is often used in embedded systems.
