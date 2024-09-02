#### **Designing for Performance:**

> [!NOTE]
> The cost of computer systems continues to drop dramatically, while the performance and capacity of those systems continue to rise equally dramatically.

- Desktop applications that require the great power of today’s microprocessor based systems include:
	- Image processing
	- Three dimensional rendering
	- Speech recognition
	- Videoconferencing
	- Multimedia authoring
	- Voice and video annotation of files
	- Simulation modeling
> [!NOTE]
> **Cloud service providers** use massive high performance banks of servers to satisfy high volume, high transaction rate applications for a broad spectrum of clients.


#### 
> [!TIP]
> chip makers can release a new generation of chips every three years with four times the number of transistors This leads to an increase in speedspeed.

#### **Techniques built into contemporary processors to increase performance include:**
- Pipelining
- Superscalar execution
- Branch prediction
- Speculative execution
- Data flow analysis

#### **[[#^74ae08|Pipelining]]:**

> [!NOTE]
> - This technique is beneficial when the amount of data to be transferred is very large, and we send the data by dividing them into various parts.
> - It facilitates parallelism in execution at the hardware level.
> - instructions arithmetic load/store conditional branch can be executed independently.

> [!WARNING]
> Pipelining **does not** reduce the execution time of individual instructions but reduces the overall execution time required for a program.

- The functionalities of pipelining in the computer networks:
	- High Performance
	- Efficient use of resources
	- Time Efficiency
	- Fast Data Delivery
	- Reduces the process waiting time

#### **Superscalar execution:**
- ! The ability to issue multiple independent instructions in parallel in every processor clock cycle
- ! Multiple parallel pipelines are used.

#### **[[#^dcc7d0|Branch prediction]]:**
- ! The processor looks ahead in the fetched instruction code and makes a prediction to maintain smooth instruction flow in the pipeline.
- ! If the prediction is incorrect, the speculatively executed instructions are discarded, and the pipeline restarts with the correct branch, resulting in a delay.

#### **Speculative execution:**

> [!NOTE]
> Using branch prediction and data flow analysis, some processors speculatively execute instructions ahead of their actual appearance in the program execution, *holding the results in temporary locations*, and *keeping execution engines as busy as possible*.

#### **Data flow analysis:**

> [!NOTE] 
> The processor analyzes which instructions are dependent on each other’s results, or data, to create an optimized schedule of instructions.

#### **Performance Balance:**

> [!NOTE]
> - One difficulty in designing an efficient system is that *different components* operate at *different speeds*.
> - It is necessary to adjust the organization and architecture to compensate for this mismatch.

> [!WARNING]
> The overall balance in the system is more important than the raw performance of any one component.

- To overcome the imbalance between memory and processor speeds there are several approaches:
	- ! Change the DRAM interface to make it more efficient by including a cache or other buffering scheme on the DRAM chip.
	- ? Increase the number of bits that are retrieved at one time by making DRAMs “ wider ” rather than “deeper” and by using wide bus data paths 8, 16, 32, and 64 bit systems.
	- ! Increase the interconnect bandwidth between processors and memory by using higher speed buses and a hierarchy of buses to buffer and structure data flow.
	- ? Reduce the frequency of memory access by incorporating increasingly complex and efficient cache structures between the processor and main memory( memory hierarchy).

#### **Improvements in Chip Organization and Architecture:**
- @ **Increase hardware speed of the processor:**
    - Achieved by shrinking the size of logic gates.
    - More gates can be packed tightly, allowing for a higher clock rate.
    - Signal propagation time is reduced.
- @ **Increase size and speed of caches:**
    - Part of the processor chip is dedicated to cache.
    - This results in significantly reduced cache access times.
- @ **Change processor organization and architecture:**
    - Aimed at increasing the effective speed of instruction execution.
    - Emphasizes parallelism to enhance performance.

#### **Problems with Clock Speed and Login Density:**
- Traditionally, the dominant factor in performance gains has been increases in clock speed due and logic density.
- However, as clock speed and logic density increase, a number of obstacles become more significant.
- Power:
	- As the density of logic and the clock speed on a chip increase, so does the power density.
	- The difficulty of dissipating the heat generated on high density, high speed chips is becoming a serious design issue.
- [[#^c689df| RC delay]]:
	- [[#^466716|R]]
	- [[#^c1f669|C]]
	- As components on the chip decrease in size, the wire interconnects become thinner, increasing resistance.
	- Also, the wires are closer together, increasing capacitance.
- Memory latency:
	- Memory speeds lag processor speeds.

#### **New approach to improving performance:**
- have turned to a fundamentally new approach to improving performance:
	- ! [[#^50dc24|Multucore]].
	- ! Many Integrated Core ( MIC ).
	- ! Graphics Processing Unit (GPU).

> [!NOTE]
> - The use of multiple processors on the same chip provides the potential to increase performance *without increasing the clock rate*.
> - With more than one healer, *the number of caches increased*.

> [!TIP]
> - Strategy is to use two simpler processors on the chip rather than one more complex processor.
> - As caches became larger it made performance sense to create two and then three levels of cache on a chip


#### **MIC & GPU:**

|   **Feature**    |                          **Many Integrated Core (MIC)**                          |                       **Graphics Processing Unit (GPU)**                        |
| :--------------: | :------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------: |
|  **Core Count**  |                       *A large number of cores per chip.*                        |          *Multiple general-purpose processors plus specialized cores.*          |
| **Performance**  | *High performance with challenges in software development to utilize all cores.* |         *High performance for graphics rendering and video processing.*         |
| **Architecture** |     *Homogeneous collection of general-purpose processors on a single chip.*     |     *Includes GPUs and specialized cores for tasks like video processing.*      |
| **Primary Use**  |                  *General-purpose processing with many cores.*                   |         *Encoding and rendering 2D/3D graphics, and processing video.*          |
| **Application**  |                *Focus on parallelism in general computing tasks.*                | *Used as vector processors for applications requiring repetitive computations.* |

#### **Basic Measures of Computer Performance:**
- **Key Considerations**: *Performance is an essential factor in evaluating computers, along with cost, size, security, reliability, and power consumption.*
- **Importance of Performance**: *Actual performance in executing specific applications is more critical than raw speed alone.*
- **Traditional Measures of Processor Speed**:
    - **Clock Speed**:
        - Determined by the pulse frequency of the system clock.
        - Measured in cycles per second (Hertz).
    - **Instruction Execution Rate**:
        - Processors execute various instructions, each requiring a specific number of cycles.

#### **Definitions:**
1. **Pipelining:** *is the process of sending multiple data packets serially without waiting for the previous acknowledgment.* ^74ae08
2. **Branch prediction:** *is a technique used in CPUs to <u>improve processing speed</u> by predicting which <u>instructions or branches will be executed next</u>, especially in pipelined processors where branching instructions can cause delays. * ^dcc7d0
3. **R:** *resistance the difficulty an electrical current has in passing through a conducting material.* ^466716
4. **C:** *capacitance the degree to which an insulating material holds a charge.* ^c1f669
5. **RC delay:** *the delay in signal speed through the circuit wiring as a result of these two effects.* ^c689df
6. **Multicore:** *multiple processors on the same chip, with a large shared cache.* ^50dc24