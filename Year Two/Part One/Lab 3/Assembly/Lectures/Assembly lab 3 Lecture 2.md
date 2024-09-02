#### The Internal Architecture of 8086:
- Units:
	- [[#^422380|BIU]]
	- [[#^e9dcb4|EU]]
- Buses:
	- [[#^8646db|Address Bus]]
	- [[#^53d2b4|Data Bus]]
	- [[#^ab5575|Control Bus]]
- [[CO Chapter 1#^e994b0|Registers]] (called segment registers) 16bit:
	- **[[#^00118f|ES]]:** *holds the base address for the Extra Segment.*
	- **[[#^9c7cd7|CS]]:** *holds the base address for the Code Segment.*
	- **[[#^977d84|SS]]:** *holds the base address for the Stack Segment.*
	- **[[#^487c00|DS]]:** *holds the base address for the Data Segment.*
	- ==**Note:**== *Each SEGMENT is 64 KB in LENGTH.*
- Address Generation Circuit:
	- It generates the 20-bit physical address using Segment base address and Offset address stored in the instruction pointer.
	- Physical Address = Segment Base Address x 10H + Offset Address
- [[#^4ab6b5|QR]]:
	- This unit is made up of 6 [[CO Chapter 1#^e994b0|registers]].
	- Each register is 8 bits in width.
- [[#^cbfcea|IP]]:
	- [[#^cbfcea|IP]] is incremented after every instruction byte is fetched.
	- [[#^cbfcea|IP]] gets a new value whenever a branch instruction occurs.
#### Advantages of memory Segmentation?
- It increases execution and fetching speeds.
- It provides a powerful memory management mechanism.
- It allows the use of 16 bit registers to give an addressing capability of 1 Megabytes. Without segmentation, it would require 20 bit registers.



#### The [[#^e9dcb4|EU]]:
- Consists of:
	- [[#^3cad33|CU]]
	- [[#^893e17|DU]]
	- [[CO Chapter 1#^f6d67f|ALU]]
	- [[#^5e0cff|FR/SR]]
	- [[#^12f05e|GPRs]]
	- [[#^efd6dc|SPRs]]
- Responsible for:
	- Telling the [[#^422380|BIU]] from where to fetch the next instruction/ data.
	- Fetching instructions from [[#^53d1c0|QR]] in [[#^422380|BIU]].
	- Decoding arithmetic and logic operations (via the [[#^893e17|DU]])
	- Executing arithmetic and logic operations (via the  [[CO Chapter 1#^f6d67f|ALU]]).

#### Flags/ status register (FR):
 - This register is 16 bits in width. 9 of the 16 bits are for the flags which stores status information about the result of the previous operation done by the ALU.
 - The flags are of 2 types:
	 - Conditional/ status flags
		1. [[#^f963bb|CF]]
		2. [[#^98068e|PF]]
		3. [[#^cca1e7|AF]]
		4. [[#^eb1322|ZF]]
		5. [[#^b1078e|SF]]
		6. [[#^5e10c0|OF]]
	- Control flags
		1. [[#^e894ee|TF]]
		2. [[#^efcae8|IF]]
		3. [[#^b91ddf|DF]]

#### General purpose registers (GPRs):
> [!NOTE]
> There are 4 general registers in the 8086 microprocessor: AX, BX, CX, and DX. Each register is 16 bits in width and is divided into two 8 bits parts (higher and lower) as shown below.

- **What are GPRs used for?**
	- ? AX register: (Combination of AL and AH Registers)
		- It holds operands and results during Arithmetical operations. Also an accumulator during String operations.
	- ? BX register: (Combination of BL and BH Registers)
		- It holds the memory address (offset address) in indirect addressing modes.
	- ? CX register: (Combination of CL and CH Registers)
		- It holds the count for instructions like a loop, rotates, shifts and string operations.
	- ? DX register: (Combination of DL and DH Registers)
		- It is used with AX to hold 32-bit values during multiplication and division.
> [!TIP]
> In general: GPRs are used to temporarily store data to increase the speed of accessing data because data stored in GPRs could be accessed much faster than if they were stored in the ROM.
#### Definitions:
1. **Address bus:** *20 bits in width therefore can address up to 1 MB of memory, and is used to send the memory address of the instruction or data being read or written.* ^8646db
2. **Data bus:** *16 bits in width and responsible for transferring data between the microprocessor and memory or I/O devices.* ^53d2b4
3. **Control bus:** *It is used to transfer control signals between the microprocessor and other components in the computer system. The control bus is used to send signals such as read, write, and interrupt requests, and to transfer status information between the microprocessor and other components.* ^ab5575
4. **[[#^53d1c0|QR]]:** *It allows to prefetch the next instructions while the processor is executing the current instruction.* ^4ab6b5
5. **[[#^d5c154|IP]]:** *It is a 16-bit [[CO Chapter 1#^e994b0|registers]] (more like a counter). It holds offset of the next instructions in the Code Segment. Therefore its content is called the “offset/ displacement”.* ^cbfcea
6. **[[#^3cad33|CU]]:** *It is responsible for directing the internal operations within the microprocessor through control signals.*
7. **[[#^893e17|DU]]:** *It is responsible for decoding arithmetic and logic operations brought from the ROM.*
8. **[[CO Chapter 1#^f6d67f|ALU]]:** *It is responsible for executing 8 and 16-bit arithmetic and logic operations.*
9. **[[#^801628|CF]]:** *Indicates when an arithmetic operation generates a carry or a borrow out of the most significant bit.* ^f963bb
10. **[[#^b0c475|PF]]:** *Shows if the number of set bits in the result is even (parity is even) or odd (parity is odd).* ^98068e
11. **[[#^04a8bd|AF]]:** *Set when a carry or borrow occurs between the lower nibble (4 bits) of an 8-bit number.* ^cca1e7
12. **[[#^8c805c|ZF]]:** *Set if the result of an operation is zero.* ^eb1322
13. **[[#^34d148|SF]]:** *Reflects the sign of the result; set if the result is negative.* ^b1078e
14. **[[#^ef8032|OF]]:** *Set when an arithmetic operation produces a result too large for the destination operand.* ^5e10c0
15. **[[#^b91ddf|TF]]:** *Allows the CPU to operate in single-step mode for debugging.* ^e894ee
16. **[[#^f82582|IF]]:** *Controls the handling of interrupts; when set, the CPU recognizes external interrupts.* ^efcae8
17. **[[#^4e3f13|DF]]:** *Determines the direction of string operations; set for decrementing and clear for incrementing.*
#### Abbreviations:
1. **BIU:** Bus Interface Unit. ^422380
2. **EU:** Execution Unit. ^e9dcb4
3. **ES:** Extra Segment Register. ^00118f
4. **CS:** Code Segment Register. ^9c7cd7
5. **SS:** Stack Segment Register. ^977d84
6. **DS:** Data Segment Register. ^487c00
7. **QR:** Queue Register Unit. ^53d1c0
8. **IP:** Instruction Pointer. ^d5c154
9. **CU:** Control Unit. ^3cad33
10. **DU:** Decoding Unit. ^893e17
11. **FR/SR:** Flags/ Status Register. ^5e0cff
12. **GPRs:** General Purpose Registers.  ^12f05e
13. **SPRs:** Special Purpose Registers. ^efd6dc
14. **CF:** Carry Flag. ^801628
15. **PF:** Parity Flag. ^b0c475
16. **AF:** Auxiliary Carry Flag. ^04a8bd
17. **ZF:** Zero Flag. ^8c805c
18. **SF:** Sign Flag. ^34d148
19. **OF:** Overflow Flag. ^ef8032
20. **TF:** Single Step Trap Flag/ Trap Flag. ^b91ddf
21. **IF:** Interrupt Flag. ^f82582
22. **DF:** Direction Flag. ^4e3f13