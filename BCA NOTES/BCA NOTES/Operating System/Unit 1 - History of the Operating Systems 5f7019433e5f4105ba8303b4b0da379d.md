# Unit 1 - History of the Operating Systems

- An **Operating System** is a program that works as an intermediary/interface between the user of a computer and the computer hardware.
- It is not possible to run any computer or mobile device without having an operating system.

### Features of Operating System

- **Convenience**
- **Memory Management**
- **Processor Management and Program Execution**
- **Device Management/I/O operation**
- **Communication**
- **Error Detection/handling**
- **Security and Reliability**

### Uses of Operating Systems

- Manage the computer’s resources, such as *Central Processing Unit, Memory, Disk drives and printers*.
- Establish a User Interface
- Execute and provide services for applications software.

### Applications of Operating System

1. Embedded Systems
2. Automobile engine controllers system
3. Industrial robots, Medical Robots and Research
4. Spacecraft Control System
5. Industrial Control
6. Large-scale computing systems such as green computing, mobile computing, soft computing, etc
7. Diagnostic mode of a computer operating system (OS)
8. Real time systems used in *Aviation, ATC system,* systems that provide immediate updating, Defense application systems like *RADAR*, Networked Multimedia Systems, and Command Control Systems.

### Evolution Of Operating System

| Generation | **Year** | **Electronic Devices used** | **Types of OS and devices** |
| --- | --- | --- | --- |
| First | **1945-55** | **Vacuum tubes** | **Plug Board** |
| Second | **1955-65** | **Transistors** | **Batch Systems** |
| Third | **1965-1980** | **Integrated circuits (IC)** | **Multiprogramming** |
| Fourth | **Since 1980** | **Large scale Integration** | **PC** |
- **CP/M :** stands for “**Central Program for microcomputers**” was almost the first OS developed for microcomputer platform based on *Intel 8080* machine in 1974 by Gary . Initially it was developed only as a file system to support all the file related operations for *PL/M (High level Programming language for 8080 machine)* compiler.
- **Proprietary Operating System :** Proprietary term describes something owned by a specific individual or company. Usually proprietary software like operating system is “*closed source*”. It is designed, customized, developed and sell by only one company. For ex : MAC OS X operating system for apple machines by Apple company.
    - Some of the features of the Proprietary OS are simplified User experience; complex graphics, limited customizability, interoperability, development and resource support from manufacturer.
- **DOS/MS-DOS :** A company called “*Seattle Computer*” developed an OS called QDOS for intel 8086 m/c. Later Microsoft Corporation acquired rights to it and developed MS-DOS (Microsoft Disk Operating System) OS.
    - **The main features of MS-DOS are :**
    1. Is is a character user interface (CUI) based OS.
    2. It is a command line operating system
    3. It supports single-user, single-tasking
    4. It is a 16-bit OS
- **UNIX, LINUX :** UNIX was initially developed as a single user operating system. It was developed much before Microsoft developed DOS. The design of DOS is based on UNIX operating system. It is popular because of features like multiple user support simultaneously, It is a CUI based OS that supports multiprogramming, time-sharing and multitasking.
- Later **LINUX** an open sourced OS was developed based on features on UNIX. It doesn’t need license and it follows open development model which allows any programmers to access the source code and modify operating system. Apart from supporting UNIX features it provides high security and cross-platform capabilities.
- **Microsoft Windows and others :** Microsoft’s windows family consists of various GUI based OS like *Windows 95, Windows 98, Windows NT, Windows 2000, Windows XP and latest versions.* The most popular windows OS currently in use are windows XP and its latest versions like Windows 8, Windows 10 which supports greater networking capabilities, user friendliness, more stability and security.

<aside>
💡 Some higher versions of operating system can be customized for parallel processing and advanced graphics capabilities, portability and interoperability and distributed environment.

</aside>

### Command Line to GUI

- A **command line interface (CLI)** is a text based user interface (UI) used to view and manage computer files. Before the mouse, users interacted with an operating system (OS) or application with a keyboard.
- The software that handles the command line interface is called **shell**, also commonly referred to as **Command Language Interpreter.**
- The CLI commands were difficult to remember and it lacked user friendliness.
- The **Graphical User Interface (GUI)** is the most popular user interface today. A GUI uses windows, menus and icons to execute commands. The advantage of GUI is, it provides pictorial/visual view of the available functions and its simple and easy to use.

### Client-Server

- **Client OS** : It is an operating system that operated within desktop. It is used to obtain services from a server. It runs on the client devices like laptop, computer and is very simple operating system.
- **Server OS** : It is an operating system that is designed to be used on server. Is is used to provide services to multiple clients. It can serve multiple clients at a time and is very advanced operating system.
    - Client/Server communication involves mainly two components, namely a client and server. They are usually multiple clients in communication with a single server.

### Types of OS

- **Batch Operating System :** In the era of 1970s, the Batch processing was very popular. The Jobs were executed in batches. People were used to have a single computer which was called mainframe. In Batch
operating system, access is given to more than one person; they submit their respective jobs to
the system for the execution.
    - The system put all of the jobs in a queue on the basis of first come first serve and then execute jobs one by one.
    - When a job completes execution, its memory is released and the output for the job gets copied
    into an output spool for later printing. Spooling is similar to buffer queue where all the
    printing operations/job are put in order.
        
        ![batchos.png](Unit%201%20-%20History%20of%20the%20Operating%20Systems/batchos.png)
        

---

- **Multiprogramming Operating System :** is an extension to the batch processing system where the CPU is always kept busy. Each process needs two type of system time : *CPU time and IO time.* In multiprogramming environment, for the time a process does its I/O, The CPU can start the execution of other processes. Therefore , it improves efficiency.
    - When two or more programs are in memory at the same time, sharing the processor is
    referred to the multiprogramming operating system. Multiprogramming assumes a
    single processor that is being shared. It increases CPU utilization by organizing jobs
    so that the CPU always has one to execute. Fig shows the memory layout for a
    multiprogramming system.
        
        ![multiOS.png](Unit%201%20-%20History%20of%20the%20Operating%20Systems/multiOS.png)
        

---

- **Time Sharing Systems :** Time sharing system supports interactive users. It is also called multitasking. It is logical extension of multiprogramming. Time sharing system uses CPU scheduling and multiprogramming to provide an economical interactive system of two or more users.
    - A time shared operating system uses CPU scheduling and multiprogramming to provide each with a small portion of a shared computer at once. Each user has least one separate program in memory. A program loaded into memory and executes, it performs a short period of time either before completion or to complete I/O. The short period of time during which user gets attention of CPU is known as time slice, time slot of quantum. It is typically of the order of 10 to 100 milliseconds.
    - Time sharing system can run several programs at the same time, so it is also a multiprogramming system. But multiprogramming operating system is not a time sharing system. Difference between both the systems is that time sharing system allows more frequent context switches. This gives each user the impression that the entire computer is dedicated to his use. In multiprogramming system a context switch occurs only when the currently executing process stalls for some reason.

---

- **Process Control & Real Time Operating System :** RTOS is an operating system intended to server real time application that process data as it comes in, mostly without buffer delay. Real time systems which were originally used to control autonomous system such as satellites, robots and hydroelectric dams. A real time operating system is one that must react to inputs and responds to them quickly. A real time operating system cannot afford to be late with a response to an event or else the output will be useless or failure.
- Real Time systems are divided into two groups : Hard real time system and Soft real time system.
    - **Hard real time system : Hard RTOS,** the deadline is handled very strictly which means that given task must start executing in specified scheduled time, and must be completed within the assigned time duration. Example : Medical critical care, Aircraft systems.
    - **Soft real time system :** is a less restrictive type. Soft RTOS, accepts some delays by the operating system. In this type of RTOS. there is a deadline assigned for a specific job. but a delay for a small amount of time is acceptable. So, deadlines are handled softly by this type of RTOS. Example : Online Transaction system and Livestock price quotation System.

---