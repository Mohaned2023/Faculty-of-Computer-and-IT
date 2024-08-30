-  **Why are we studying this course?**
	- What happens in between?
	- How is a computer designed using logic gates and wires to satisfy specific goals?
	- SW: 
		-  Problem
		- Algorithm
		- Program Language
		- Runtime System (OS)
	- ==Architecture==
	- ==Organization==
	- HW:
		- Logic
		- Circuits
		- Electronics
- **Computing System:**
	1. Computing Unit.
	2. Communication Unit.
	3. Memory/Storage Unit:
		- Memory System.
		- Storage System.
- **Von-Neumann Computer Architecture (1945):** 
	- Model for designing and building computers, based on : 
		1. The computer consists of four main sub-systems:
			1. Memory.
			2. [[#^f6d67f| ALU]]
			3. Control Unit.
			4. [[#^bdbd95| I/O]] System.
		2. Program is stored in memory during execution.
		3. Program instructions are executed sequentially.
- **System Bus:**
	1. Control Bus.
	2. Address Bus.
	3. Data Bus.
- **The fourth basic functions that a computer can perform:**
	1. Data processing.
	2. Data storage.
	3. Data movement.
	4. Control.
- **Multicore Computer Structure:**
	1. [[#^c945c9|CPU]]:
		- Portion of the computer that fetches and executes instructions.
		- Consists of an [[#^ea60d0|ALU]], a [[#^72ec86|control unit]], and [[#^e994b0|registers]].
		- Referred to as a ==processor in a system with a single processing unit==
	2. [[#^427453|Core]]:
		- May be equivalent in functionality to a [[#^c945c9|CPU]] on a single CPU system.
		- Specialized processing units are also referred to as cores.
	3. [[#^f1229b|Processor]]:
		- Is the computer component that interprets and executes instructions.
		- Referred to as a multicore processor if it contains multiple [[#^427453|cores]].
- **Cache Memory:**
	-  [[#^579b28|Cache Memory]]
	- Is smaller and faster than main memory
	- Used to speed up memory access by placing in the cache data from main memory that is likely to be used in the near future.
	- A greater performance improvement may be obtained by using multiple levels of cache, with ([[#^1a4265|L1]]) closest to the core and additional levels ([[#^396798|L2]], [[#^c13ec4|L3]], etc.) progressively farther from the core.
- Computer Evolution:
	- Brief history of computers:
		- The First Generation: ==Vacuum tubes==.
		- The Second Generation: ==Transistors==.
		- The Third Generation: ==Integrated Circuits==.
		- Later generations.
	- Embedded Systems.
	- [[#^fdb2a2|IoT]].
	- Cloud Computing.
- First Generation: Vacuum Tubes
	- Vacuum tubes were used for ==digital logic elements and memory==.
	- [[#^bcc77f|IAS]] computer:
		- Fundamental design approach was the stored program concept.
		- Design began at the Princeton Institute for Advanced studies.
		- Completed in 1952.
		- Prototype of all subsequent ==general purpose computers==.
- [[#^bcc77f|IAS]] Structure:
	- **Main memory:** which stores both ==data and instructions==.
	- **[[#^f6d67f|ALU]]:** capable of ==operating on binary data==.
	- **[[#^72ec86|Control Unit]]:** which interprets the ==instructions in memory== and ==causes them to be executed==.
	- **[[#^bdbd95|I/O]] System:** equipment operated by the control unit.
	- CPU Registers: 
		1. [[#^ad45fb|AC]]
		2. [[#^ad45fb|MQ]]
		3. [[#^e58036|MBR]]
		4. [[#^cfcef5|IBR]]
		5. [[#^5dbcf4|PC]]
		6. [[#^caf0ac|MAR]]
		7. [[#^1d92e3|IR]]
- [[#^bcc77f|IAS]] Memory Formats:
	1. Number word: ==0 for the sign and 39 for the number==.
	2. Instruction word: 
		1. Left Instruction ( 20bit ):
			1. 0-8 [[#^52a8b2|opcode]] ( 8bit ).
			1. 8-20 address ( 12bit ).
		2. Right Instruction ( 20bit ):
			1. [[#^52a8b2|opcode]] ( 8bit ).
			2. address ( 12bit )
- Microelectronics:
	- Elements of a digital computer:
		- [[#^6cd56f|Gates]] and [[#^e201f3|memory cells]].
		- By interconnecting large numbers of these fundamental devices, we can construct a computer.
- Integrated Circuits:
	- Exploits the fact that such components as transistors, resistors, and conductors can be fabricated from a semiconductor such as silicon.
	- Many transistors can be produced at the same time on a single wafer of silicon.
	- Transistors can be connected with a processor metallization to form circuits.
##### Differences between **General Purpose** computers and **Embedded Systems**:

| **Aspect**                                             | **General-Purpose Computers**                                       | **Embedded Systems**                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------|
| **User Interface**                                    | Can be complex (real-time robotic vision) or simple (flashing light) | May have no user interface or be very simple                            |
| **Diagnostic Port**                                   | Used for diagnosing the system                                      | Used for diagnosing the system being controlled                         |
| **Software**                                          | Multi-functional                                                   | Often has a fixed function, specific to the application                 |
| **Efficiency**                                        | Not always optimized                                                | Optimized for energy, code size, execution time, weight, dimensions, and cost |
| **Field Upgrades**                                    | May not be as crucial                                               | Important for fixing bugs, improving security, and adding functionality  |
##### Differences between **Computer Organization** and **Computer Architecture**:

- **Computer Organization**: ==Focuses on the physical layout== and operational mechanisms of the hardware components.
- **Computer Architecture**: ==Focuses on the logical structure== and functional design, ensuring the system performs effectively based on defined goals.

| **Aspect**               | **Computer Organization**                                                                 | **Computer Architecture**                                                                           |
| ------------------------ | ----------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| **Definition**           | Refers to how the actual physical components of a computer are organized and implemented. | Refers to the conceptual design and fundamental operational structure of a computer system.         |
| **Focus**                | Focuses on the physical components, such as circuits, memory, and input/output units.     | Focuses on designing a system that is efficient and meets performance objectives.                   |
| **Implementation**       | Deals with how instructions are actually executed in the hardware.                        | Deals with how the system is designed to achieve specific goals like performance and functionality. |
| **Level of Abstraction** | Lower level of abstraction; closer to hardware.                                           | Higher level of abstraction; closer to software and system models.                                  |
| **Examples**             | Memory management, instruction execution, physical interconnections.                      | Processor architecture, [[#^14a247\| (ISA)]], memory hierarchy design.                              |
| **Primary Concern**      | The actual performance and efficiency of the system.                                      | The functions that the system provides and how these are achieved.                                  |
| **Interaction**          | How different components interact with each other to make the device work.                | How software interacts with hardware to achieve optimal performance.                                |



#### Definitions:
1. ==**Computer:**== is a complex system; contemporary computers contain millions of Elementary electronic components.
2. ==**The hierarchical nature of complex systems:**== is essential to both their design and their description.
3. ==**Hierarchical system:**== is a set of interrelated subsystems, each of the latter, in turn, is hierarchical in structure until we reach the lowest level of the elementary subsystem.
4. ==**Structure:**== The way in which the components are interrelated.
5. ==**Function:**== The operation of each individual component as part of the structure.
6. ==**[[#^2dde01|CPU]]:**== controls the operation of the computer and performs its data processing functions. ^c945c9
7. ==**[[#^f6d67f|ALU]]:**== Performs the computer’s data processing function. ^ea60d0
8. ==**Registers:**== Provide storage internal to the  [[#^2dde01|CPU]]. ^e994b0
9. ==**Control Unit:**== Controls the operation of the [[#^2dde01|CPU]] and hence the computer. ^72ec86
10. ==**Core:**== An individual processing unit on a [[#^f1229b|processor]] chip. ^427453
11. ==**Processor:**== Physical piece of silicon containing one or more [[#^427453|cores]]. ^f1229b
12. ==**Cache Memory:**== Multiple layers of memory between the [[#^f1229b|processor]] and main memory. ^579b28
13. ==**[[#^c01aac|MBR]]:**== Contains a word to be stored in memory or sent to the [[#^bdbd95|I/O]] unit. ^e58036
14. ==**[[#^eccd12|MAR]]:**== Specifies the address in memory of the word to be written from or read into the [[#^e58036|MBR]]. ^caf0ac
15. ==**[[#^ebbabe|IR]]:**== Contains the 8 bit [[#^52a8b2|opcode]] instruction being executed. ^1d92e3
16. ==**[[#^8cfd6d|IBR]]:**== Employed to temporarily hold the right hand instruction from a word in memory. ^cfcef5
17. ==**[[#^1f634e|PC]]:**== Contains the address of the next instruction pair to be fetched from memory. ^5dbcf4
18. ==**[[#^6b6e6f|AC]] and [[#^144788|MQ]]:**== Employed to temporarily hold operands and results of [[#^ea60d0|ALU]] operations. ^ad45fb
19. ==**Data Channel:**== is an independent [[#^bdbd95|I/O]] module with its own processor and instruction set.
20. ==**Gate:**== is a device that implements a simple Boolean or logical function. ^6cd56f
21. ==**Memory Cell:**== is a device that can store 1 bit of data. ^e201f3
22. ==**Cloud Computing:**== is a culmination of numerous attempts at large scale computing with seamless access to virtually limitless resources.
#### Abbreviations:
1. **ALU:** Arithmetic/Logic Unit. ^f6d67f
2. **I/O:** Input/Output.  ^bdbd95
3. **ISA:** Instruction Set Architecture. ^14a247
4. **CPU:** Central Processing Unit. ^2dde01
5. **L1:** Level 1 of cache. ^1a4265
6. **L2:** Level 2 of cache. ^396798
7. **L3:** Level 3 of cache. ^c13ec4
8. **IoT:** Internet of Things. ^fdb2a2
9. **IAS:** Institute for Advanced studies.  ^bcc77f
10. **AC:** Accumulator Register. ^6b6e6f
11. **MQ:** Multiply-quotient Register. ^144788
12. **MBR:** Memory Buffer Register. ^c01aac
13. **IBR:** Instruction Buffer Register. ^8cfd6d
14. **PC:** Program Counter. ^1f634e
15. **MAR:** Memory Address Register. ^eccd12
16. **IR:** Insruction Register.  ^ebbabe
17. **opcode:** Operation Code. ^52a8b2
18. **CSP:** Cloud Service Provider.