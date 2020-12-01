# Answers to the Review Questions

# What are the three subsystems that make up a computer?
- CPU
- Memory
- I/O

# What are the components of a CPU?
- Computing Unit (CU)
- Arithmetic Logic Unit (ALU)
- Registers/Memory

# What is the function of the ALU?
To recieve instructions and perform logical and arithmetic operations on data

# What is the function of control unit?
To manage I/O, read instructions from the RAM and direct them to the ALU. 
In general, it manages everything in the CPU

# What is the function of main memory?
To store program instructions and data, each with a unique address.

# Define RAM, ROM, SRAM, DRAM, PROM, EPROM and EEPROM.
## RAM - Random Access Memory
Stores programs temporarily, and is volatile
Stores the majority of data on the computer

## SRAM  - Static RAM
is a type of RAM which works by switching on (1) and off (0) logic gates, and doesn't need to be refreshed
DRAM is a type of RAM which works by charging capacitors. As you read, you drain the capacitors, the content's address locations need to be refreshed

## ROM - Read Only Memory 
Permanent storage of data, and is involatile (contents are kept when the power cuts off).

 Usually contains the bootstrapper program to start the Operating System.

## PROM - Programmable ROM
ROM but manufactor can program it 

Can only be done **ONCE**

EPROM - Can be erased in special conditions (UV light)

EEPROM - Can be erased electrically

# What is the purpose of cache memory?
To be the middleman between the CPU's memory (registers) and the main memory (RAM & HDD). This is because Registers are expensive, but cache memory is faster than main memory without the extra cost

# Types of Input/Output
# Nonstorage Devices
Keyboard/Monitor/Printer

# Storage Devices
# Magnetic 
## Magnetic Disk
- Divided into tracks and sectors, Intertrack and InterSector gap between each track/sector
- Random Data Access to the beginning of each sector
- Speed Depends on several factors
	- Rotation Speed
	- Seek Time (time to move to target sector)
	- Transfer Time (Between Disk and CPU)

## Magnetic Tape
- 9 Bits, 8 for information 1 for error check
- Sequential Access
- Cheaper

# Non-Magnetic

## Describe the physical components of a magnetic disk.
One or more disks stacked with Read/Write Heads. Disks store 1 if magnitised, else 0

## How are the surfaces of a magnetic disk and magnetic tap organized?
Both are magnetic, however a magnetic disk is split into multiple tracks and sectors, with gaps between tracks and sectors. 

A Magnetic tape is a long strand of magnetic material which is generally half an inch wide, and has 9 tracks.
The first 8 vertical locations of the tracks are for storing 8 bits of information, and the 9th is for a checksum (error checking)

## Compare and contrast CD-R, CD-RW, and DVD.
TODO go over this again
CD-R
Writable only once, readable multiple times

CD-RW
Rewritable

DVD
Stores more data

## Compare and contrast SCSI, FireWire and USB controllers. (Connecting I/O Devices)
## SCSI
Can be daisy chained but needs to have terminators in the end
Each device needs to have a unique Address
Can have 8/16/+ devices depending on how wide the bus is
Paralell interface - Many bits at once

## Firewire
Serial Interface - One bit at a time & in packets
Can be Daisy Chained/Tree Connection
High speed (at the time)
63 devices with one controller (Multiple devices)

## USB
Competitor for FireWire
Universal Serial Bus - Serial not Paralell interface
Cannot be Daisy chained
For high and low speed devices?
Can connect multiple devices

## HDMI
Digitial Interface for previously Analog video standards

# Compare and contrast the two methods for handling the addressing of I/O devices.
## Isolated I/O - 
Different instructions for each/Smaller Instructions
no need to differentiate between memory and controller addresses

## Memory-Mapped I/O - 
No Seperate Instructions for each type
Memory addresses saved for I/O devices - less for the main memory


# Compare and contrast the three methods for handling the synchronization of the CPU with I/O devices.
TODO revise flowcharts

## Programmed I/O
Continously checks for I/O before proceeding
- Waits for I/O

## Interrupt Driven I/O
Do something else until an Interrupt occurs

## Direct Memory Access
DMA controller has direct accesss to memory and CPU
Good for high speed I/O
Offputs load on the CPU into the DMA Controller
DMA Controller has it's own Registers etc

# Compare and contrast CISC architecture with RISC architecture.
CISC Architecture is easier to program, as it has many more complex instructions built in. More complicated circuitry and less efficient.
However, RISC Architecture is much more simply designed. This causes it to be harder to program, however it is much more efficient, and therefore used in mobiles.

# Describe pipelining and its purpose.
Instead of doing one fetch/decode/execute at a time, do one of each at a time

Doing `n`'s execution, `n` + 1's Decode, and `n` + 2's Fetch simultaniously

this increases the throughput, (Instructions performed/time)

# Describe parallel processing and its purpose.
Used to increase throughput
Old computers -> SISD
Modern computers -> MIMD

## SISD - Single instruction-stream, single data-stream (SISD)
- One CU
- One ALU
- One Memory Unit
Very Basic, everything is sequential

## SIMD - single instruction-stream, multiple data-stream 
- One CU
- Multiple ALUs
- Multiple Memory Units
Matrix/Array data processing?
GPU uses SIMD

## MISD - multiple instruction-stream, single data-stream
Multiple instruction streams operate on the same data stream
useless, never implemented

## MIMD - multiple instruction-stream, multiple data-stream (MIMD)
True Paralell Processing Architecture
Several Tasks occuring simultaniously



