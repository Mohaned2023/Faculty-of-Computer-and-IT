#### **Memory Systems:**
- **Typical Computer System:** *is equipped with a hierarchy of memory subsystems.* ^529895
- Type of memory:
	- ! <u>Internal memory</u>, directly accessible by the processor.
	- ! <u>External memory</u>, accessible by the processor via an I/O module.

#### **Characteristics of Memory Systems:**
1. **Location:** *Refers to whether memory is internal and external to the computer.* ^dc29fa
	- Internal memory:
		1. ? main memory.
		2. ? registers.
		3. ? Cache
	- External memory: 
		- ? consists of peripheral storage devices that are accessible to the processor via <u>I/O controllers</u>.
2. **Capacity:** *Memory is typically expressed in terms of the number of words or Bytes.* ^c76758
	- @ Word size: Common word size: 8, 16, 32 bits.
3. **Unit of transfer**
	- Internal memory: ^2cd5e4
		- ! The number of bits read out of or written into memory at a time.
		- ? Usually governed by data bus width.
	- External memory: ^14ecda
		- ! Usually, a block that is much larger than a word.
	- Addressable unit:  ^74f8c0
		- ! The smallest location that can be uniquely addressed.
4. **Access Method:**
	- **Sequential access:** *Memory is organized into units of data called records.* ^1fecd3
		- ? Access must be made in a specific linear sequence.
		- ? Access time depends on the location of data and previous location, access time is variable.
		- ! e.g. tape
	- **Direct access:** *Individual blocks or records have a unique address based on physical location.* ^8d00f2
		- ? Involves a shared read write mechanism.
		- ? Access time depends on location and the previous location, access time is variable.
		- ! e.g. disk
	- **Random access:** *Individual addresses identify locations exactly.* ^666236
		- ? The time to access a given location is independent of the sequence of prior accesses and is constant.
		- ? Any location can be selected at random and directly addressed and accessed.
		- ! e.g. some cache systems and RAM
	- **Associative:** *A word is retrieved based on a portion of its contents rather than its address.* ^eb12a4
		- ? Each location has its own addressing mechanism and retrieval time is constant independent of location or prior access patterns.
		- ! e.g. Cache
5. Capacity and Performance:
	1. Access time (latency):
		- ? For random access memory it is the time it takes to perform a read or write operation.
		- ? For non random access memory it is the time it takes to position the read write mechanism at the desired location.
	2. Memory cycle time:
		- ? Access time plus any additional time required before second access can commence (Start To End).
		- ? Additional time may be required for transients to die out on signal lines or to regenerate data if they are read destructively.
		- ! Concerned with the system bus , not the processor.
	3. Transfer rate:
		- ? The rate at which data can be transferred into or out of a memory unit.
		- ? For random access memory it is equal to 1 /(cycle time).
6. Physical Type:
	1. ! Semiconductor memory: RAM & ROM
	2. ! Magnetic surface memory: Disk & Tape
	3. ! Optical: CD & DVD
	4. ! Magneto
7. Physical Characteristics:
	1. ! **Volatile memory:** *Information decays naturally or is lost when electrical power is switched off.* ^5c2e0b
	2. ! **Nonvolatile memory:** *No electrical power is needed to retain information.* ^b178c8
	3. ! **Magnetic surface memories:** *Are nonvolatile.* ^1fba74
	4. ! **Semiconductor memory:** *May be either volatile or nonvolatile.* ^308c3c
	5. ! **Nonerasable memory:** *Cannot be altered, except by destroying the storage unit Semiconductor memory of this type is known as (ROM).* ^b73340

#### **Memory Hierarchy:**
- Design constraints on a computer s memory can be summed up by three questions:
	1. ! How much
	2. ! How fast
	3. ! How expensive
- There is a trade off among capacity, access time, and cost:
	1. ! Faster access time, greater cost per bit.
	2. ! Greater capacity, smaller cost per bit.
	3. ! Greater capacity, slower access time.
> [!NOTE]
> The way out of the memory dilemma is not to rely on a single memory component or technology, but to employ a memory hierarchy.
- The goal of a memory hierarchy:
	1. @ to keep the data that is accessed most high up the hierarchy, so it can be accessed quickly.
	2. @ the least used at the bottom of the hierarchy.

#### **Disk cache:**
- ! A portion of main memory can be used as a buffer to hold data temporarily that is to be read out to disk.
- ! A few large transfers of data can be used instead of many small transfers of data.
- ! Data can be retrieved rapidly from the software cache rather than slowly from the disk.

#### **Definitions:**
1. **[[#^529895|Typical Computer System]]:** *is equipped with a hierarchy of memory subsystems.*
2. **[[#^dc29fa|Location Memory Systems]]:** *Refers to whether memory is internal and external to the computer.*
3. **[[#^c76758|Capacity Memory Systems]]:** *Memory is typically expressed in terms of the number of words or Bytes.*
4. **[[#^2cd5e4|Unit of transfer Internal memory]]:**  *The number of bits read out of or written into memory at a time.*
5. **[[#^14ecda|Unit of transfer External memory]]:** *Usually, a block that is much larger than a word.*
6. **[[#^74f8c0|Unit of transfer Addressable unit]]:** *The smallest location that can be uniquely addressed.*
7. **[[#^1fecd3|Access Method Sequential Access]]:** *Memory is organized into units of data called records.*
8. **[[#^8d00f2|Access Method Direct Access]]:** *Individual blocks or records have a unique address based on physical location.*
9.  **[[#^666236|Access Method Random access]]:** *Individual addresses identify locations exactly.*
10. **[[#^eb12a4|Access Method Associative]]:** *A word is retrieved based on a portion of its contents rather than its address.*
11. **[[#^5c2e0b|Physical Characteristics Volatile memory]]:** *Information decays naturally or is lost when electrical power is switched off.*
12. **[[#^b178c8|Physical Characteristics Nonvolatile memory]]:** *No electrical power is needed to retain information.*
13. **[[#^1fba74|Physical Characteristics Magnetic surface memories]]:** *Are nonvolatile.*
14. **[[#^308c3c|Physical Characteristics Semiconductor memory]]:** *May be either volatile or nonvolatile.*
15. **[[#^b73340|Physical Characteristics Nonerasable memory]]:** *Cannot be altered, except by destroying the storage unit Semiconductor memory of this type is known as (ROM).*
