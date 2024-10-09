### **Physical Characteristics of Disk Systems:**
- @ Head Motion:
	- Fixed head (one per track).
	- Movable head (one per surface).
- @ Disk Portability:
	- Nonremovable disk.
	- Removable disk.
- @ Sides:
	- Single sided.
	- Double sided.
- @ Platters:
	- Single platter.
	- Multiple platter.
- @ Head Mechanism:
	- Contact (floppy).
	- Fixed gap.
	- Aerodynamic gap (Winchester).

### **Physical Characteristics of Disk Systems:**
- @ **Head Motion:**
	- Fixed-head disk:
		- ? One read-write head per track.
		- ? Heads are mounted on a fixed ridged arm that extends across all tracks.
	- Movable-head disk: 
		- ? One read/write head per side
		- ? Head is mounted on an arm
		- ? The arm can be extended or retracted
- @ **Disk Portability:**
	- Non-removable disk:
		- ? Permanently mounted in the drive.
		- ? Hard disk.
	- Removable disk: 
		- Can be removed from drive and replaced with another disk.
		- Provides unlimited storage capacity.
		- Easy data transfer between systems.
- @ **Sides:**
	- Single sided:
		- ? Some less expensive disk systems use single-sided disks.
	- Double-sided:
		- ? Magnetisable coating is applied to both sides of the platter.
- @ **Platters:** 
	- Single platter.
	- Multiple platter.

### **Solid State Drives (SSD) Compared to HDD:**
- @ High-performance input/output operations per second.
- @ Durability.
- @ Longer lifespan.
- @ Lower power consumption.
- @ Quieter and cooler running capabilities.
- @ Lower access times and latency rates.

### **Addressing Modes:**
- @ Immediate.
- @ Direct.
- @ Indirect.
- @ Register.
- @ Register indirect.
- @ Displacement.
- @ Stack.

### **Immediate Addressing:**
- ? Simplest form of addressing.
- ? Operand = A
- ! The operand is specified in the instruction <u>explicitly</u>.
- ? Instead of an address field, an operand field is present that contains the operand.
- ! This mode can be used to define and <u>use constants or set initial values of variables</u>.
- @ Advantage:
	- ? No memory reference other than the instruction fetch is required to obtain the operand.
- @ Disadvantage:
	- ? The size of the number is restricted to the size of the address field, which, is small compared with the word length.

### **Direct Addressing:**
- ? Effective address (EA) = address field A.
- ! The address field of the instruction <u>contains</u> the effective address of the <u>operand</u>.
- ? Only one reference to memory is required to fetch the operand.
- @ Advantage:
	- ? Requires only one memory reference and no special.
- @ Disadvantage:
	- ? Limitation is that it provides only a limited address space.

### **Indirect Addressing:**
- ? EA = (A)
- ? Parentheses are to be interpreted as meaning contents of.
- ? The address field of the instruction specifies the address of the memory location that contains the effective address of the operand.
- @ Advantage:
	- ? Availability of large address space.
- Disadvantage:
	- ? Instruction execution requires two memory references to fetch the operand.
	- ? One to get its address and a second to get its value.

### **Register Addressing:**
- ? EA = R
- ? The operand is contained in a register set.
- ! Address field refers to a register <u>rather</u> than the main memory address.
- @ Advantage:
	- ? <u>No reference</u> to memory is required to fetch the operand.
- @ Disadvantage:
	- ? The address space is very <u>limited</u>.

### **Register Indirect Addressing:**
- ? EA = (R)
- ? The address field of the instruction refers to a CPU register that contains the effective address of the operand in the memory.
- @ Advantage:
	- ? Availability of large address space.
- @ Disadvantage:
	- ? One reference to memory is required to fetch the operand.
### **Displacement Addressing:**
- ? Combines the <u>capabilities</u> of direct addressing and register indirect addressing.
- ? Requires that the instruction have <u>two address fields</u>, at least one of which is <u>explicit</u>
- @ Most common uses:
	- ! Relative addressing.
	- ! Base-register addressing.
	- ! Indexing.

### **Relative Addressing:**
- ? EA = A + (PC)
- ! The <u>implicitly</u> referenced register is the program counter (PC)
- ? The next instruction address is added to the address field to produce the EA.
- ! The <u>effective address</u> of the operand is obtained by <u>adding</u> the content of the program counter (PC) with the address part of the instruction.
- ! The effective address is a <u>displacement</u> relative to the <u>address of the instruction</u>.

### **Base-Register Addressing:**
- ? EA = A + (R)
- ! Effective address of the operand is <u>obtained</u> by adding the content of the base register with the address part of the instruction.
- ? For base-register addressing, the interpretation is the following:
	- The referenced register contains the main memory address, and the address field contains a displacement (usually an unsigned integer representation) from that address.
	- The register reference may be explicit or implicit.

### **Indexing Addressing:**
- ? EA = A + (R)
- ! Effective address of the operand is <u>obtained</u> by adding the content of the index register with the address part of the instruction.
- ? The address field references the main memory address and the referenced register contains a positive displacement from that address.
- ? An important use is to provide an efficient mechanism for performing iterative operations.

### **Stack Addressing:**
- ? A stack is a linear array of locations:
	- ! Sometimes referred to as lastin-first-out queue.
- ? A stack is a reserved block of locations.
	- ! Items are appended to the top of the stack so that the block is partially filled.

### **Applications of Addressing Modes:**

|                           Addressing Modes                           | Applications                                                                                                                                                                                                                       |
| :------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                      Immediate Addressing Mode                       | - To initialize registers to a constant value                                                                                                                                                                                      |
|   Direct Addressing Mode<br>and<br>Register Direct Addressing Mode   | - To access static data<br>- To implement variables                                                                                                                                                                                |
| Indirect Addressing Mode<br>and<br>Register Indirect Addressing Mode | - To implement pointers because pointers are memory locations that store the address of another variable<br>- To pass anarray as a parameter because thearray name is the base address and apointer is needed to point the address |
|                       Relative Addressing Mode                       | - To change the normal sequence of execution of instructions<br>- For branch type instructions since it directly updates the program counter                                                                                       |
|                    Base Register Addressing Mode                     | - Implementation of relocatable code i.e. relocation of program in memory even at run time<br>- For handling recursive procedures                                                                                                  |
|                        Index Addressing Mode                         | - For array implementation or array addressing<br>- For records implementation                                                                                                                                                     |

### **Addressing mode calculation:**
- ! Virtually all computer architectures provide <u>more than</u> one of these addressing modes.
- ! How the processor can <u>determine</u> which address mode is being used in a particular instruction?
> [!NOTE]
> <u>One or more</u> bits in the instruction format can be used as a mode <u>field</u>. The value of the mode field determines which addressing mode is to be used.

