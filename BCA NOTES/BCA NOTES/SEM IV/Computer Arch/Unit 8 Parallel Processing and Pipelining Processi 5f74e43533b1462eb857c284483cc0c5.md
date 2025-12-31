# Unit 8 : Parallel Processing and Pipelining Processing

### Comparison of Uniprocessors and Parallel processors

- A uniprocessor system is defined as a computer system that has a single central processing unit that is used to execute computer tasks.
- As more and more modern software is able to make use of multiprocessing architectures, such as SMP and MPP, the term uniprocessor is therefore used to distinguish the class of computers where all processing task share a single CPU.
- Most desktop computers are now shipped with multiprocessing architectures. As such, this kind of system uses a type of architecture that is based on a single computing unit.
- Parallel processing is a method in computing of running two or more processors (CPUs) to handle separate parts of an overall task.
- Breaking up different parts of a task among multiple processors will help reduce the amount of time to run a program.
- Any system that has more than one CPU can perform parallel processing, as well as multi-core processors which are commonly found on computers today.

<aside>
💡 **In an SMP system, each processor shares the same resources.** **In an MPP system, each processor has its own dedicated resources and shares nothing, In an SMP system, each processor shares the same resources.** **In an MPP system, each processor has its own dedicated resources and shares nothing**

</aside>

### EPIC

- **EPIC :** Explicitly Parallel Instruction Computing
- EPIC (Explicitly Parallel Instruction Computing) is a 64-bit microprocessor instruction set which is an improvement to the VLIW (Very Large Instruction Word) architecture.
- It provides up to 128 general and floating point unit registers and uses speculative loading, predication, and explicit parallelism to accomplish its computing tasks.
- By 1989, researchers at HP recognized that reduced instruction set computer (RISC) architectures were reaching a limit at one instruction per cycle. They began an investigation into a new architecture named EPIC.
- One goal of EPIC was :
    - to move the complexity of instruction scheduling from the CPU hardware to the software compiler
    - exploit instruction level parallelism (ILP) by using the compiler to find and exploit
    additional opportunities for parallel execution

### Evolution of Parallel Processing

- Parallel processing is a form of information processing involving concurrency techniques to
achieve more efficient computing systems.
- There are five generations till now, beginning from 1940s
1. First Generation (1939-1954): The first generation marks the development of computer
systems utilizing a technology of vacuum tubes. This generation was marked with several
developments because of the ongoing World War II. ENIAC, Mark III, UNIVAC, Clyde (tube
computers) were built in this time.
2. Second Generation (1954-1959): The second generation saw the development of
transistor technology, and IBM introduced the first solid state computers. It was also the
generation of SSI and MSI (Small and Medium Scale Integrated) circuits.
3. Third Generation (1959-1971): Texas Instruments patented first integrated circuits. The
first minicomputer, PDP-8 was introduced. Project ARPANET was introduced. Intel
developed first Large Scale Integrated (LSI) circuits.
4. Fourth Generation (1971-1991): VLSI (Very Large Scale Integrated) circuits were
introduced. This helped reduce cost of computers greatly. Microprocessors were
developed. This generation also marked the rise of Apple, Microsoft and Nintendo.
5. Fifth Generation (1991-Present): World Wide Web (by Tim Berners Lee, CERN) and
browsers (Mosaic, Netscape Navigator, Explorer) were introduced

### Parallel Processing Architecture

- There are multiple types of parallel processing, two of the most commonly used types include SIMD and MIMD.
- SIMD, or single instruction multiple data, is a form of parallel processing in which a
computer will have two or more processors follow the same instruction set while each processor handles different data.
- SIMD is typically used to analyze large data sets that are based on the same specified benchmarks.
- MIMD, or multiple instruction multiple data, is another common form of parallel processing which each computer has two or more of its own processors and will get data from separate data streams.
- Classification of Parallel Processor Architecture :

![parallel.PNG](Unit%208%20Parallel%20Processing%20and%20Pipelining%20Processi/parallel.png)

### SIMD & MIMD

- **SIMD - Single Instruction Multiple Data**
    - Main features of the architecture
    - Large number of small or simple processors.
    - Each Processor has its own memory
    - A single “control processors” issues each instruction, in turn every processor executes the same instruction on its local data at the same time.
    - Some processor may be turned off on any instruction. This allows certain logical operations to be performed
- **MIMD - Multiple Instruction Multiple Data**
    - In computing , MIMD is a technique employed to achieve parallelism.
    - Machines using MIMD have a number of processors that function asynchronously and independently.
    - At any time, different processors may be executing different instructions on different pieces of data.
    - MIMD architectures may be used in a number of application areas such as computer-aided design/computer-aided manufacturing, simulation, modeling, and as communication switches.
    - MIMD machines can be of either shared memory or distributed memory categories.
    - These classifications are based on how MIMD processors access memory. Shared memory machines may be of the bus-based, extended, or hierarchical type. Distributed memory machines may have hypercube or mesh interconnection schemes.

### Overview of Parallel Processing & Pipelining Processing

- Parallel processing is a method in computing of running two or more processors (CPUs) to handle separate parts of an overall task.
- Breaking up different parts of a task among multiple processors will help reduce the amount of time to run a program.
- Any system that has more than one CPU can perform parallel processing, as well as multi-core processors which are commonly found on computers today.
- Parallel processing is commonly used to perform complex tasks and computations.
- Working of Parallel Processing :
    - Typically, a computer scientist will divide a complex task into multiple parts with a software tool and assign each part to a processor, then each processor will solve its part, and the data is reassembled by a software tool to read the solution or execute the task.
    - Typically, each processor will operate normally and will perform operations in parallel as instructed, pulling data from the computer’s memory.
    - Processors will also rely on software to communicate with each other so they can stay in sync concerning changes in data values.
    - Assuming all the processors remain in sync with one another, at the end of a task, software will fit all the data pieces together.
    - Computers without multiple processors can still be used in parallel processing if they are networked together to form a cluster.
- Pipeline Processing
    - The processor execute the program by fetching and executing instructions.
    - One after the other.
    Let Fi and Ei refer to the fetch and execute steps for instruction I
    
    ![Pipeline.PNG](Unit%208%20Parallel%20Processing%20and%20Pipelining%20Processi/Pipeline.png)
    
- Computer that has two separate hardware units, one for fetching and another for executing them.
- the instruction fetched by the fetch unit is deposited in an intermediate buffer B1.
- This buffer needed to enable the execution unit while fetch unit fetching the next
instruction.
- The computer is controlled by a clock.
- Any instruction fetch and execute steps completed in one clock cycle

### High Performance Computing

- High Performance Computing (HPC) evolved due to meet increasing demands for processing speed.
- HPC beings together several technologies such as computer architecture, algorithms, programs and electronics and system software under a single canopy to solve advanced problems effectively and quickly.
- A highly efficient HPC system requires a high-bandwidth, low-latency network to connect multiple nodes and clusters.