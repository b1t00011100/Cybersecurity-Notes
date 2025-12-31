# Unit 7 : Memory Management

## Introduction

- In a uni-programming system, main memory is divided into two parts : one part for the operating system(resident, monitor, kernel) and one part for the program currently being executed.
- In a multiprogramming system, the “user” part of memory must be further subdivided to accommodate multiple processes.
- The task of subdivision is carried out dynamically by the OS and is known as **Memory Management.**

---

### Contiguous Memory Allocation

- Contiguous memory allocation is a memory allocation method that allocates a single contiguous section of memory to a process or a file.
- Analyzes the requirement of the storage for that particular file or process and then allocated accordingly i.e sufficient contiguous memory block.

---

### Memory Allocation

- The main memory has to accommodate both the OS and the user space.
- In Contiguous memory allocation, when the process arrives from the ready queue to the main memory for execution, the contiguous memory blocks are allocated to the process according to its requirement. Now, to allocate the contiguous space to user processes, the memory can be dividing either in the fixed-sized partition or in the variable-sized partition.
    - **Fixed-size Partition :** In the *fixed size partition*, the memory is divided into fixed-sized blocks and each block contains exactly one process. But, the fixed size partition will limit the degree of multiprogramming as the number of partition will decide the number of processes.
    - **Variable-sized Partition :** In the *variable sized partition,* the OS maintains a table that contains the information about all memory parts that are occupied by the processes and all memory parts that are still available for the processes.

---

### Fixed Partitioned Memory Management

<aside>
💡 This is the oldest and simplest technique used to put more than one processes in the main
memory. In this partitioning, number of partitions (non-overlapping) in RAM are fixed but
size of each partition may or may not be same. As it is contiguous allocation, hence no
spanning is allowed. Here partition are made before execution or during system configure.

</aside>

- As illustrated in above figure, first process is only consuming 1MB out of 4MB in the main
memory.
- Hence, Internal Fragmentation in first block is (4-1) = 3MB. Sum of Internal Fragmentation
in every block = (4-1)+(8-7)+(8-7)+(16-14)= 3+1+1+2 = 7MB
- Suppose process P5 of size 7MB comes. But this process cannot be accommodated inspite of
available free space because of contiguous allocation (as spanning is not allowed). Hence,
7MB becomes part of External Fragmentation.

![FPMM.PNG](Unit%207%20Memory%20Management/FPMM.png)

- Advantages of Fixed Partitioning
    1. **Easy to Implement**
    2. **Little OS overhead -** Processing of Fixed Partitioning require lesser excess and indirect computational power.
- Disadvantages of Fixed Partitioning
    1. **Internal Fragmentation -** Main memory use is inefficient. Any program, no matter how small, occupies an entire partition.
    2. **External Fragmentation -** The total unused space of various partitions cannot be used to load the processes even though there is space available, but not in the contiguous form.
    3. **Limit process size**
    4. **Limit on Degree of Multiprogramming -** Partition in Main Memory are made before execution or during system configure. Number of processes greater than number of partitions in RAM is invalid in Fixed Partitioning.

---

### Dynamic Partitioning

- To overcome fixed partitioning , an approach known as dynamic partitioning was developed.
- When a process is brought into main memory, it is allocated as much memory as it requires and no more.
- **Relocation :** refers to the process of moving a program from one memory space to another during allocation
    
    ---
    

### Paging

- Both unequal fixed-size and variable-size partitions are inefficient in the use of memory; the former results in internal fragmentation, the latter in external fragmentation.
- Suppose, however, that main memory is partitioned into equal fixed-size chunks that are relatively small, and that each process is also divided into small fixed-size chunks of the same size.
- Then the chunks of a process, known as pages, could be assigned to available chunks of memory, known as frames, or page frames.
    
    ---
    

### Segmentation

- A process is divided into segments, which are all not necessarily of the exact sizes are called segments.
- **Base Address :** Starting point of one dimensional physical address
- **Offset :** LIMIT