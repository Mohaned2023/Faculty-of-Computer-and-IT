### **Register Organization:**
- ? Within the processor there is a <u>set of registers</u> that function as a level of memory above main memory and cache in the hierarchy.
- @ The registers in the processor perform two roles:
	- ! **User-Visible Registers:** *Enable the machine or assembly language programmer to minimize main memory references by <u>optimizing use of registers</u>.* ^8d4dc1
	- ! **Control and Status Registers:** *Used <u>by the control unit</u> to control the operation of the processor and <u>by operating system</u> programs to control the execution of programs.* ^d7187e

### **User-Visible Registers:**
- ? A user-visible register may be referenced by the <u>machine language</u> that the processor executes.
- @ Categories:
	- ! General purpose
	- ! Data
	- ! Address
	- ! Condition codes: Also referred to as flags

### **Control and Status Registers:**
- @ Four registers are essential to instruction execution:
	- ? Program counter (PC)
	- ? Instruction register (IR)
	- ? Memory address register (MAR)
	- ? Memory buffer register (MBR)

### **Program Status Word (PSW):**
- ! **Program Status Word:** *register or set of registers that contain status information.* ^688002
- @ Common fields or flags include:
	- ? Sign Zero.
	- ? Carry.
	- ? Equal.
	- ? Overflow.
	- ? Interrupt Enable/Disable.

### **Factors to limit Pipelining performance:**
- ? If the stages are <u>not of equal</u> duration, there will be some waiting involved at various pipeline stages.
- ? Another difficulty is the <u>conditional branch instruction</u>, which can invalidate several instruction fetches.
- ! An interrupt.

### **Types of Data Hazard:**
- ? Read after write (RAW), or true dependency.
- ? Write after read (WAR), or antidependency.
- ? Write after write (WAW), or output dependency.

### **Control Hazard:**
- ? Also known as a branch hazard.
- ? Occurs when the pipeline makes the <u>wrong decision on a branch prediction</u>, Brings instructions into the pipeline that must subsequently be discarded.
- @ An approaches have been taken for dealing with conditional branches:
	- ! Multiple streams.
	- ! Prefetch branch target.
	- ! Loop buffer.
	- ! Branch prediction.
	- ! Delayed branch.

### **Definitions:**
1. User-Visible Registers: [[#^8d4dc1|Here]].
2. Control and Status Registers: [[#^d7187e|Here]].
3. Program Status Word: [[#^688002|Here]].