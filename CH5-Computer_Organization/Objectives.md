# Computer Organization - Objectives

## List the three subsystems of a computer.
- CPU
- Main Memory
- Input/Output

## Describe the role of the central processing unit (CPU).
Performs operations on data, and contains the ALU, CU, and Registers

### Arithmetic Logic Unit - ALU
Performs three main operations:
#### Logic 
Working with bits eg. NOT/AND/OR/XOR

#### Mathematical Operations 
(Arithmetic) eg. ADD, SUB 

#### Shifting of bits 
eg. Logical Right/Left, Arithmetic Right/Left, Circular Right/Left

### Registers
Registers are memory which are inside the CPU

As a result, this type of memory is very fast

Of the registers described, you have:
#### Data Registers
Holds the input data and results of operations

#### Instruction Registers
Stores the current instruction, eg, `ADD Register10, Register11`

#### Program Counter
**NOT THE INSTRUCTION REGISTER**

Keeps track of the location of the current instruction.

Example:
```
10| ADD r10, r11 <-- Current Instruction
11| XOR r10, r11
12| AND r10, r13
```
Then, the current instruction is completed, and the counter is `incremented`
```
10| ADD r10, r11
11| XOR r10, r11 <-- Current Instruction
12| AND r10, r13
```

### Control Unit - CU
Controls the operation of other subsystems (Memory & I/O) via signals

## Describe the main memory and its addressing space.
A collection of storage locations, each having their own unique `address`.

Storing every individual bit would require an enormous amount of memory!

Therefore, we store the location of `words` instead, which are a group of bits. 

When data is written or read, it is done as an entire `word`

## Memory Hierarchy
Balance between speed and price

Registers are inside the CPU, fastest and most $$$

Cache is in between the memory and registers, containing data frequently used

Main Memory is slowest but cheapest

## Define the input/output subsystem.
Allows the computer to communicate with the outside world

Can be split into two categories

### Non-Storage Devices
- Keyboards
- Monitors
- Mice
- Printers

### Storage Devices
[Details here](answers.md)
- Magnetic Disks
- Magnetic Tape
- Optical Storage


## Understand the interconnection of subsystems.
The subsystems are interconnected by connections, called a `bus`

### There are 3 main kinds of bus
#### Data Bus
Paralell connections (1 connection per bit)

Each bit is transmitted at the same time

Bits Required:
```
Depends on the size of a word
if a word was 32 bits:
32 bits -> 32 connections
```

#### Address Bus
Specifies the word being accessed

Bits Required:
```
Depends on the number of words
if there are 256 words:
256 -> 2^8
We can represent 256 addresses as an 8 bit unsigned integer
```

#### Control Bus
Specifies the control action, or operation to be taken

Ex. Read or Write

Bits Required:
```
Depends on the number of operations
For example, if we have 7 operations required
Round up to a power of 2, which is 8
8 -> 2^3
So we can represent 8 operations in 3 bits
```

## Controllers (Not in Objectives)
[Details here](answers.md)

## Describe different methods of input/output addressing.
The same bus is used to read and write to memory

There are two methods for I/O addressing:
### Isolated I/O
Overlap in memory locations
Different instructions for memory and I/O devices, no clashes

### Memory-Mapped I/O
No Overlap, No Seperate Instructions

+ Less Instructions
- More Connections in the Bus

## Describe the fetch-decode-execute phases of a cycle.

### Fetch
Retrieve the next instruction referenced by the instruction counter
Increment the instruction counter

### Decode
Decode the instruction into binary?
TODO isn't the instruction already in binary

### Execute
Send instruction to the relevant component
Eg. 
- `LOAD` value from **Memory**
- `ADD` values of two registers in the **ALU**

## Distinguish the two major trends in the design of computers.
### CISC & RISC
[Details here](answers.md)

## Understand how computer throughput can be improved using pipelining and parallel processing.
[Details here](answers.md)


[Back to Main Page](../README.md)