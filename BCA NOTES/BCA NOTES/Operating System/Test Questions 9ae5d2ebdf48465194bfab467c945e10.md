# Test Questions

- **What is OS ? Need of OS .**
    - An **Operating System** is a program that works as an intermediary/interface between the user of a computer and the computer hardware.
    - Operating system (OS) manages all of the software and hardware on the computer.
    - It performs basic tasks such as file, memory and process management, handling input and output, and controlling peripheral devices such as disk drives and printers.
    - It is not possible to run any computer or mobile device without having an operating system.
    - Need for Operating System :
        - **OS as a platform for Application programs:** The operating system provides a platform, on top of which, other programs, called application programs can run. These application programs help users to perform a specific task easily.
        - **Managing Input-Output unit:** The operating system also allows the computer to manage its own resources such as memory, monitor, keyboard, printer, etc. Management of these resources is required for effective utilization. The operating system controls the various system input-output resources and allocates them to the users or programs as per their requirements.
        - **Multitasking:** The operating system manages memory and allows multiple programs to run in their own space and even communicate with each other through shared memory.
- **Operating System Objectives and Functions.**
    - An **Operating System** is a program that works as an intermediary/interface between the user of a computer and the computer hardware.
    - Objectives of OS :
        - To hide the details of the hardware resources from the users.
        - To provide users a convenient interface to use the computer system.
    - Functions of OS :
        - The main function of the operating system is that it allocates resources and services, such as memory, processors, information and devices.
        - It also includes the program that handles these resources like a memory management module, I/O programs, a file system and a traffic controller.
        - The process of starting or restarting the computer is known as booting. If the computer is switched off completely and if turned on then it is called cold booting. Warm booting is a process of using the operating system to restart the computer
        - The operating system uses password protection to protect user data and similar other techniques. it also prevents unauthorized access to programs and user data. The operating system provides various techniques which assure the integrity and confidentiality of user data.
- **Explain different types of Operating Systems**
    - Different Types of Operating System are :
        - **Batch Operating System :** In the era of 1970s, the Batch processing was very popular. The Jobs were executed in batches. People were used to have a single computer which was called mainframe. In Batch operating system, access is given to more than one person; they submit their respective jobs to the system for the execution.
        - **Multiprogramming Operating System :** is an extension to the batch processing system where the CPU is always kept busy. Each process needs two type of system time : *CPU time and IO time.* In multiprogramming environment, for the time a process does its I/O, The CPU can start the execution of other processes. Therefore , it improves efficiency.
        - **Time Sharing Systems :** Time sharing system supports interactive users. It is also called multitasking. It is logical extension of multiprogramming. Time sharing system uses CPU scheduling and multiprogramming to provide an economical interactive system of two or more users.
        - **Process Control & Real Time Operating System :** RTOS is an operating system intended to server real time application that process data as it comes in, mostly without buffer delay. Real time systems which were originally used to control autonomous system such as satellites, robots and hydroelectric dams.
- **Explain layered Structure of OS with diagram.**
    - The structure of the OS depends mainly on how the various common components of the operating system are interconnected and melded into the kernel.
    - The layered structure approach breaks up the operating system into different layers and retains much more control on the system.
    
    - The bottom layer (layer 0) is the hardware, and the topmost layer (layer N) is the user interface.
    - These layers are so designed that each layer uses the functions of the lower-level layers only.
    - It simplifies the debugging process as if lower-level layers are debugged, and an error occurs during debugging. The error must be on that layer only as the lower-level layers have already been debugged
    
    ![layered-structure-of-operating-system.png](Test%20Questions/layered-structure-of-operating-system.png)
    
- **What is System Call? Some examples of system calls.**
    - A system call is a method for a computer program to request a service from the kernel of the operating system on which it is running.
    - A system call is a method of interacting with the operating system via programs. A system call is a request from computer software to an operating system's kernel.
    - The **Application Program Interface (API)** connects the operating system's functions to user programs.
    - The kernel system can only be accessed using system calls, System calls are required for any programs that use resources.
    - Some examples of system calls are read, open, write, close, wait, exec, fork, exit and kill.
    - There are hundreds of systems calls in many contemporary operating systems.
- **Difference between thread and process.**
    
    
    | **S.NO** | **Process** | **Thread** |
    | --- | --- | --- |
    | **1.** | Process means any program is in execution. | Thread means a segment of a process. |
    | **2.** | The process takes more time to terminate. | The thread takes less time to terminate. |
    | **3.** | It takes more time for creation. | It takes less time for creation. |
    | **4.** | It also takes more time for context switching. | It takes less time for context switching. |
    | 5. | Multiprogramming holds the concepts of multi-process. | We don’t need multi programs in action for multiple threads because a single process consists of multiple threads. |
    | 6. | The process is called the heavyweight process. | A Thread is lightweight as each thread in a process shares code, data, and resources. |
    | 7. | A system call is involved in it. | No system call is involved, it is created using APIs. |
    | 8. | The process does not share data with each other. | Threads share data with each other. |
- **PCB with its roles, structure & hierarchy.**
    - **Process Control Block** is used to track the process’s execution status. Each block of memory contains information about the process state, program counter, stack pointer, status of opened files, scheduling algorithms, etc.
    
    1. **Pointer:** It is a stack pointer that is required to be saved when the process is switched from one state to another to retain the current position of the process.
    2. **Process state:** It stores the respective state of the process.
    3. **Process number:** Every process is assigned a unique id known as process ID or PID which stores the process identifier.
    4. **Program counter:** It stores the counter**:** which contains the address of the next instruction that is to be executed for the process.
    5. **Register:** These are the CPU registers which include the accumulator, base, registers, and general-purpose registers.
    6. **Memory limits:** This field contains the information about memory management system used by the operating system. This may include page tables, segment tables, etc.
    7. **Open files list** **:** This information includes the list of files opened for a process.
    
    ![process-table.jpg](Test%20Questions/process-table.jpg)
    
- **What is Process State with its diagram.**
    1. **New:** Newly Created Process (or) being-created process.
    2. **Ready:** After the creation process moves to the Ready state, i.e. the process is ready for execution.
    3. **Run:** Currently running process in CPU (only one process at a time can be under execution in a single processor)
    4. **Wait (or Block):** When a process requests I/O access.
    5. **Complete (or Terminated):** The process completed its execution.
    6. **Suspended Ready:** When the ready queue becomes full, some processes are moved to a suspended ready state
    7. **Suspended Block:** When the waiting queue becomes full.
- **What is Critical Section Problem?**
    - Critical Section is the part of a program which tries to access shared resources. That resource may be any resource in a computer like a memory location, Data structure, CPU or any IO device.
    - The critical section cannot be executed by more than one process at the same time; operating system faces the difficulties in allowing and disallowing the processes from entering the critical section.
    - The critical section problem is used to design a set of protocols which can ensure that the Race condition among the processes will never arise.
    - In order to synchronize the cooperative processes, our main task is to solve the critical section problem. We need to provide a solution in such a way that the following conditions can be satisfied.
    - Requirement for Synchronization mechanisms
    - **Mutual Exclusion :** By Mutual Exclusion, we mean that if one process is executing inside critical section then the other process must not enter in the critical section.
    - **Progress :** Progress means that if one process doesn't need to execute into critical section then it should not stop other processes to get into the critical section.
    - **Bounded Waiting :** We should be able to predict the waiting time for every process to get into the critical section. The process must not be endlessly waiting for getting into the critical section.
    
- **What is Race condition?**
    - A race condition is an undesirable situation that occurs when a device or system attempts to perform two or more operations at the same time.
    - The Race Condition is a condition which usually occurs in Multi Threading concept.
    - The Race Condition also occurs in the case of processes also. If we do not take care of this Race Condition well then we might get stuck in a Deadlock too.
    - **Race condition in Multi-Thread Scenario :** A race condition is a situation that develops when many threads share a resource or execute the same piece of code in a multithreaded context. Inappropriate handling of this might result in an unfavorable scenario where the output state depends on the threads execution order.
    - **Race condition in Multi-Processing Scenario** : The Race Condition is a situation that is developed when a device or system tries to do two or more operations simultaneously, the actions must be performed in the right order to be performed successfully; a race condition is an unpleasant circumstance that results.
    - **Race condition in Critical Section Problem :** A race condition is a potential scenario that might happen within a critical section area. This occurs when different results from the execution of numerous threads in a crucial region are obtained depending on the execution order of the threads.
- **What is semaphore? and its algorithm to avoid critical section problem.**
    - Semaphores are integer variables that are used to solve the critical section problem by using two atomic operations, wait and signal that are used for process synchronization.
    - The definitions of wait and signal are as follows −
    - **Wait**
        
        The wait operation decrements the value of its argument **S**, if it is positive. If **S** is negative or zero, then no operation is performed.
        
        ```python
        wait(S)
        {
           while (S<=0);
        
           S--;
        }
        ```
        
    - **Signal**
        
        The signal operation increments the value of its argument **S**.
        
        ```python
        signal(S)
        {
           S++;
        }
        ```
        
- **Explain different types of Schedulers**
    - Process scheduling is the activity of the process manager that handles the removal of the running process from the CPU and the selection of another process on the basis of a particular strategy.
    - There are three types of Process Schedulers
    - **Long-Term or Job Schedulers :** It brings the new process to the ‘Ready State’. It controls the ***Degree of Multi-programming***, i.e., the number of processes present in a ready state at any point in time. It is important that the long-term scheduler make a careful selection of both I/O and CPU-bound processes
    - **Short-Term or CPU Scheduler :** It is responsible for selecting one process from the ready state for scheduling it on the running state.
        - NOTE : Short-term scheduler only selects the process to schedule it doesn’t load the process on running. Here is when all the scheduling algorithms are used.
    - **Medium-Term Scheduler :**  It is responsible for suspending and resuming the process. It mainly does swapping (moving processes from main memory to disk and vice versa). Swapping may be necessary to improve the process mix or because a change in memory requirements has overcommitted available memory, requiring memory to be freed up. It is helpful in maintaining a perfect balance between the I/O bound and the CPU bound. It reduces the degree of multiprogramming.
- **Explain peterson’s algorithm for mutual exclusion.**
    
    -NOTEBOOK NOTES!!!
    
- **Explain Round Robin algorithm**
    - **Round Robin** is a CPU scheduling algorithm where each process is assigned a fixed time slot in a cyclic way. It is basically the preemptive version of First come First Serve CPU Scheduling algorithm.
    - Round Robin CPU Algorithm generally focuses on Time Sharing technique.
    - The period of time for which a process or job is allowed to run in a pre-emptive method is called time **quantum**.
    - Each process or job present in the ready queue is assigned the CPU for that time quantum, if the execution of the process is completed during that time then the process will **end** else the process will go back to the **waiting table** and wait for its next turn to complete the execution.
    - Working of Round Robin algorithm -
        1. All the processes are added to the ready queue.
        2. At first, The burst time of every process is compared to the time quantum of the CPU.
        3. If the burst time of the process is **less than or equal** to the time quantum in the round-robin scheduling algorithm, the process is executed to its burst time.
        4. If the burst time of the process is **greater than** the time quantum, the process is executed up to the time quantum (TQ).
        5. When the time quantum expires, it checks if the process is executed completely or not.
        6. On completion, the process terminates. Otherwise, it goes back again to the *ready state*.