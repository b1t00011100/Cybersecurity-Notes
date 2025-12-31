# Unit 2-Operating System : Functions and Structures

## Different Services of Operating Systems

An Operating System supplies different kinds of services to both the user and to the programs as well. The Common services provided by the operating systems are explained below:

### Process Management

- Process refers to a program in execution. The process management is a procedure for
managing the many processes that are running simultaneously on the operating system.
- A process needs certain resources such as CPU time, memory, files and I/O devices. This can be given to the process when it is created or allocated while running.
- When the process terminates the Operating system will reclaim its reusable resources.
- The OS is responsible for the following activities of the process management :
    1. Creating and destroying the user and system processes.
    2. Allocating hardware resources among the processes.
    3. Controlling the progress of processes.
    4. Providing mechanism for process communication.
    5. Also provides mechanisms for deadlock handling.

---

### Main Memory Management

- Main Memory is a large array of storage or bytes, which has an address. The memory management process is conducted by using a sequence of reads or writes of specific memory addresses. In order to execute a program, it should be mapped to absolute addresses, and loaded inside the memory. For a program to be executed, it must be in the Main memory.
- The memory management modules of an operating system are concerned with the
management of the primary (main memory) memory. Memory management is concerned
with following functions:
    1. Keeping track of the status of each location of main memory. I.e. each memory location is either free or allocated.
    2. Determining allocation policy for memory
    3. Allocates the memory when a process requests. Allocation techniques are used to choose specific location. It is also responsible for allocation information updating.
    4. It also de-allocates the Memory when a process no longer requires or has been terminated. After de-allocation, status information must be updated
- **Secondary Memory Management :** A storage device is a mechanism by which the compute may store information in such a way that this information may be retrieved at a later time. Secondary storage device is used for storing all the data and programs. These programs and data access by computer system must be kept in main memory. Size of Main memory is small to accommodate all data and programs. It also loses when the data when power goes off, for this reason secondary storage is required.

---

### File Management

- Logically related data items on the secondary storage are usually organized into named collections called files.
- A file may contain a report, an executable program or a set of commands to the operating system. A file consists of a sequence of bits, bytes, lines or records whose meanings are defined by their creators. For this, Physical media (Secondary Storage) is used.
- Physical media are of two different types : Magnetic disk and Optical Media.
- The Operating system is responsible for the following in connection with file management:
    1. Creating and destroying files.
    2. Mapping files onto secondary storage.
    3. Creating and deleting directories.
    4. Backing up files on stable storage media.
    5. Supporting primitives for manipulating files and directories.
    6. Transmission of file elements between main and secondary storage.

---

### Uses of System Calls

> A system call is a mechanism that provides the interface between a process and the operating system. It is a programmatic method in which a computer program requests a service from the kernel of the OS. If a file system requires the creation of deletion of files, Reading and writing from files also requires a system call. System calls offers the services of the OS to the user program via API. System calls are the only entry points for the kernel system.
> 

<aside>
💡 System Calls = User Mode —> Kernel Mode

</aside>

- Services Provided by System calls
    1. Process Creation and Management.
    2. Main memory Management
    3. File Access, Directory and file system management
    4. Device Handling
    5. Protection
    6. Networking
- There are 5 Types of System Calls
    1. Process control/creation and management:
        1. Create Process
        2. Terminate Process
        3. Wait
        4. Fork
        5. End
        6. Abort
        7. Load
        8. Execute
        9. Get and process attributes
        10. Allocate and Free Memory
    2. File Access, Directory and File system management : 
        1. Create File
        2. Open File to read or write
        3. Delete file
        4. Stat : get information about a file
        5. unlink : remove file from a directory
        6. get and set file attributes
    3. I/O Device management
        1. Request device : To ensure exclusive use of device
        2. Release device : Release the device after the execution
        3. Read/Write : Same as file system call
        4. Stat : Get information about I/O devices
    4. Information maintenance
        1. Get time and date
        2. Set time and date
        3. Get process, file or device attributes
        4. Set process, file or device attributes
        5. Get system data
        6. Set system data
    5. Inter Process communication
        1. Create message queue
        2. Send message
        3. Receive message
        4. Close connection

---

## Operating System Structure

> The design of operating system architecture traditionally follows the separation of concerns principle. The Principle suggests structuring the OS into relatively independent parts the provide simple individual features, thus keeping the complexity of the design manageable
> 

### A kernel

- A **Kernel** is the core component of an operating system. A kernel is an important part of an OS that manages system resources. It also acts as a bridge between software and hardware of the computer.
    
    Kernel of an OS
    
    ![data_center-kernel_layout.png](Unit%202-Operating%20System%20Functions%20and%20Structures/data_center-kernel_layout.png)
    
- There are various types of kernel namely *Monolithic kernel, Microkernel, hybrid kernel, Exo-Kernel, and Nano-Kernel.* Most widely used kernel is Monolithic Kernel and Microkernel. Kernel space is where the kernel executes and provides its services. User space is that set of memory locations in which the user processes run.
1. **Monolilthic (Simple) Operating System :** Monolithic kernel manages system resources between application and hardware, but user services and kernel services are implemented under same address space. It increases the size of the kernel, thus increases size of operating system as well. This kernel provides CPU scheduling, memory management, file management and other operating system functions through system calls.
    
    ![Desktop Screenshot 2023.09.11 - 19.34.00.01.png](Unit%202-Operating%20System%20Functions%20and%20Structures/Desktop_Screenshot_2023.09.11_-_19.34.00.01.png)