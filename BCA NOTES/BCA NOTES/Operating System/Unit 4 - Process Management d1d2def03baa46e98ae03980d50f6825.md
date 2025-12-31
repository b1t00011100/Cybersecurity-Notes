# Unit 4 - Process Management

## Introduction

- A process is a program in execution. For example : When we write a program in C or C++ and compile it, the compiler creates binary code. The Original code and binary Code are both programs. When we run it, it becomes a **process.**
- A **Process** is an ‘active‘ entity instead of a program, which is considered a ‘passive’ entity.
- **Process management** refers to the techniques and strategies used by organizations to design, monitor, and control their business processes to achieve their goals efficiently and effectively.
- Process management includes various tools and techniques such as process mapping, process analysis, process improvement, process automation, and process control. By applying these tools and techniques, organizations can streamline their processes, eliminate waste, and improve productivity.
- If the OS supports multiple users then services under this are very important. In this regard OS have to keep track of all the completed processes, Schedule them and dispatch them one after another. But the user should feel that he has full control of the CPU.
    - Some of the system calls in this category are :
        1. Create a child’s process identical to the parent’s
        2. Terminate a process
        3. Wait for a child process to terminate
        4. Change the priority of the process
        5. Block the process
        6. Ready the process
        7. Dispatch the process
        8. Suspend the process
        9. Resume the process
        10. Delay a process
        11. Fork a process

## Process

### What does a process look like in a memory?

- **Text Section :** A process, sometimes known as the text section, also includes the current activity represented by the value of the program counter.
- **Stack :** The stack contains temporary data, such as function parameters, return addresses, and local variables.
- **Data Section :** Contains the global variable.
- **Heap Section :** Dynamically allocates memory to the process during its run time.

![process.png](Unit%204%20-%20Process%20Management/process.png)

---

### Attributes of a Process

- **Process ID** : A unique identifier assigned by the operating system.
- **Process State** : Can be ready, running ,etc.
- **CPU Registers :** Like the Program Counter (CPU registers must be saved and restored when a process is swapped in and out of the CPU).
- **Accounts information :** Amount of CPU used for process execution, time limit, execution ID, etc.
- **I/O status information :** For example, devices allocated to the process, open files, etc.
- **CPU scheduling information :** For example, Priority (Different processes may have different priorities, for example, a shorter process assigned high priority in the shortest job first scheduling).

<aside>
☕ These all attributes are a part of PCB (Process Control Block), Every Process has its own PCB.

</aside>

### Process Control Block

- Process Control Block is used to track the process’s execution status. Each block of memory contains information about the process state, program counter, stack pointer, status of opened files, scheduling algorithms, etc.

1. **Pointer:** It is a stack pointer that is required to be saved when the process is switched from one state to another to retain the current position of the process.
2. **Process state:** It stores the respective state of the process.
3. **Process number:** Every process is assigned a unique id known as process ID or PID which stores the process identifier.
4. **Program counter:** It stores the counter,**:** which contains the address of the next instruction that is to be executed for the process.
5. **Register:** These are the CPU registers which include the accumulator, base, registers, and general-purpose registers.
6. **Memory limits:** This field contains the information about memory management system used by the operating system. This may include page tables, segment tables, etc.
7. **Open files list** **:** This information includes the list of files opened for a process.

![process-table.jpg](Unit%204%20-%20Process%20Management/process-table.jpg)

---

### States of Process

- A process is in one of the following states :

1. **New:** Newly Created Process (or) being-created process.
2. **Ready:** After the creation process moves to the Ready state, i.e. the process is ready for execution.
3. **Run:** Currently running process in CPU (only one process at a time can be under execution in a single processor)
4. **Wait (or Block):** When a process requests I/O access.
5. **Complete (or Terminated):** The process completed its execution.
6. **Suspended Ready:** When the ready queue becomes full, some processes are moved to a suspended ready state
7. **Suspended Block:** When the waiting queue becomes full.

![process-states1.png](Unit%204%20-%20Process%20Management/process-states1.png)

---

## Context Switching

- **Context Switching** in an operating system involves saving the context or state of a running process so that it can be restored later, and then loading the context or state of another process and run it.
- **Example –** Suppose in the OS there (N) numbers of processes are stored in a Process Control Block. like The process is running using the CPU to do its job. While a process is running, other processes with the highest priority queue up to use the CPU to complete their job.

### Need for Context Switching

- Context switching enables all processes to share a single CPU to finish their execution and store the status of the system’s tasks. The execution of the process begins at the same place where there is a conflict when the process is reloaded into the system.

### State Diagram of Context Switching

![swapping1.png](Unit%204%20-%20Process%20Management/swapping1.png)

### Working of Context Switching

1. The state of the current process must be saved for rescheduling.
2. The process state contains records, credentials, and operating system-specific information stored on the PCB or switch.
3. The PCB can be stored in a single layer in kernel memory or in a custom OS file.
4. A handle has been added to the PCB to have the system ready to run.
5. The operating system aborts the execution of the current process and selects a process from the waiting list by tuning its PCB.
6. Load the PCB’s program counter and continue execution in the selected process.
7. Process/thread values can affect which processes are selected from the queue, this can be important.

## Process Scheduling

- Process scheduling is the activity of the process manager that handles the removal of the running process from the CPU and the selection of another process on the basis of a particular strategy.
- Process scheduling is an essential part of a Multiprogramming operating system. Such operating systems allow more than one process to be loaded into the executable memory at a time and the loaded process shares the CPU using time multiplexing .

---

### Categories in Scheduling

- **Non-preemptive -** In this case, a process’s resource cannot be taken before the process has finished running. When a running process finishes and transitions to a waiting state, resources are switched.
- **Preemptive -** In this case, the OS assigns resources to a process for a predetermined period of time. The process switches from running state to ready state or from waiting for state to ready state during resource allocation, Basically Context Switching.

---

### Process Schedulers

- **Long-Term or Job Schedulers :** It brings the new process to the ‘Ready State’. It controls the ***Degree of Multi-programming***, i.e., the number of processes present in a ready state at any point in time. It is important that the long-term scheduler make a careful selection of both I/O and CPU-bound processes
- **Short-Term or CPU Scheduler :** It is responsible for selecting one process from the ready state for scheduling it on the running state.
    - NOTE : Short-term scheduler only selects the process to schedule it doesn’t load the process on running. Here is when all the scheduling algorithms are used.
- **Medium-Term Scheduler :**  It is responsible for suspending and resuming the process. It mainly does swapping (moving processes from main memory to disk and vice versa). Swapping may be necessary to improve the process mix or because a change in memory requirements has overcommitted available memory, requiring memory to be freed up. It is helpful in maintaining a perfect balance between the I/O bound and the CPU bound. It reduces the degree of multiprogramming.

## Multithreading

- A **thread** is a path which is followed during a program’s execution.
    - For example a program is not capable of reading keystrokes while making drawings. These tasks cannot be executed by the program at the same time. This problem can be solved through multitasking so that two or more tasks can be executed simultaneously.
- Multitasking is of two types :
    1. **Processor based :** Processor based multitasking is totally managed by the OS.
    2. **Thread based :** Thread based or multithreading can be controlled by the programmer to some extent.
- The concept of **multi-threading** needs proper understanding of these two terms – **a process and a thread**. A process is a program being executed. A process can be further divided into independent units known as threads. A thread is like a small light-weight process within a process.

![thread-1.jpg](Unit%204%20-%20Process%20Management/thread-1.jpg)

### Implementation of Threads

- **User Level Threads :** In this model, the operating system does not directly support threads. Instead, threads are managed by a user-level thread library, which is part of the application. The library manages the threads and schedules them on available processors. The advantages of user-level threads include greater flexibility and portability, as the application has more control over thread management. However, the disadvantage is that user-level threads are not as efficient as kernel-level threads, as they rely on the application to manage thread scheduling.
- **Kernel Level Threads :** In this model, the operating system directly supports threads as part of the kernel. Each thread is a separate entity that can be scheduled and executed independently by the operating system. The advantages of kernel-level threads include better performance and scalability, as the operating system can schedule threads more efficiently. However, the disadvantage is that kernel-level threads are less flexible and portable than user-level threads, as they are managed by the operating system.

---

### Models of Multithreading

- There are three Models in Multithreading.

- **Many to Many Model -** In this model, we have multiple user threads multiplex to same or lesser number of kernel level threads. Number of kernel level threads are specific to the machine, advantage of this model is if a user thread is blocked we can schedule others user thread to other kernel thread. Thus, System doesn’t block if a particular thread is blocked.

![many_to_many1-300x200.jpg](Unit%204%20-%20Process%20Management/many_to_many1-300x200.jpg)

- **Many to One Model -** In this model, we have multiple user threads mapped to one kernel thread. In this model when a user thread makes a blocking system call entire process blocks. As we have only one kernel thread and only one user thread can access kernel at a time, so multiple threads are not able access multiprocessor at the same time.

![many_to_many2-300x200.jpg](Unit%204%20-%20Process%20Management/many_to_many2-300x200.jpg)

- **One to One Model -** In this model, one to one relationship between kernel and user thread. In this model multiple thread can run on multiple processor. Problem with this model is that creating a user thread requires the corresponding kernel thread.

![many_to_many3-300x200.jpg](Unit%204%20-%20Process%20Management/many_to_many3-300x200.jpg)