# Unit 6 : I/O Management & Deadlock

## Introduction

- I/O software are often organized in the following layers ➖

- **User Level Libraries :** This provides simple interface to the user program to perform input and output. For Ex - **Stdio** is a standard library provided by C and C++ Programming languages.
- **Kernel Level Modules :** This provides device driver to interact with the device controller and device independent I/O module used by the device driver.
- **Hardware :** This layer includes the actual hardware and hardware controller which interact with the device driver and makes hardware alive.

![os IO mangement.PNG](Unit%206%20I%20O%20Management%20&%20Deadlock/os_IO_mangement.png)

<aside>
💡 A key concept in the design of I/O software is that it should be device independent where it
should be possible to write programs that can access any I/O device without having to specify
the device in advance

</aside>

---

### Device Drivers

- Device drivers are software modules that can be plugged into an OS to handle a particular device.
- OS takes help from device drivers to handle all I/O devices.
- Device Drivers encapsulate device-dependent code and implement a standard interface in such a way that code contains device-specific register reads/writes.
- The Device Driver performs the following jobs :
    - To accept request from the device independent software above to it.
    - Interact with the device controller to take and give I/O and perform required error handling.
    - Making sure that the request is executed successfully.

---

### Interrupt Handlers

- An **interrupt handler,** also known as interrupt service routine or ISR, is a piece of software or more specifically a callback function in an OS or more specifically in a device driver, whose execution is triggered by the reception of an interrupt.
- When the interrupt happens, the interrupt procedure does whatever it has to in order to handle the interrupt, updates data structures and wakes up process that was waiting for an interrupt to happen.
- This interrupt mechanism accepts an address — a number that selects a specific interrupt handling routine from a small set. In most architectures, this address is an offset stored in a table called the interrupt vector table. This vector contains the memory addresses of specialized interrupt handlers.

---

### Device-Independent I/O Software

- The basic function of the device-independent software is to perform the I/O functions that are common to all devices and to provide a uniform interface to the user-level software.
- Though it is difficult to write completely device independent software but we can write some modules which are common among all the devices.
- Following is a list of functions of device independent I/O Software —
    - Uniform interfacing for device drivers
    - Device naming - Mnemonic names mapped to major and minor device numbers.
    - Device Protection
    - Providing a device independent block size
    - Buffering because data coming off a device cannot be stored in final destination.
    - Storage allocation on block devices
    - Allocation and releasing dedicated devices
    - Error Reporting

---

### User - Space I/O Software

- These are the libraries which provide richer and simplified interface to access the functionality of the kernel or ultimately interactive with the device driver.
- Most of the user-level I/O software consists of library procedures with some exception like spooling system which is a way of dealing with dedicated I/O devices in a multiprogramming system.
- For ex : I/O Libraries (e.g., stdio) are in user-space to provide an interface to the OS resident device- independent I/O SW. For example putchar(), getchar(), printf() and scanf() are example of user level I/O library stdio available in C programming.

---

### Kernel I/O Subsystem

- Kernel I/O Subsystem is responsible to provide many services related to I/O. Following are some of the service provided :
    - **Scheduling :** Kernel schedules a set of I/O requests to determine a good order in which to execute them. When an application issues a blocking I/O system call, the request is placed on the queue for that device. The Kernel I/O scheduler rearranges the order of the queue to improve the overall system efficiency and the average response time experienced by the applications.
    - **Buffering :**  Kernel I/O Subsystem maintains a memory area known as buffer that stores data while they are transferred between two devices or between a device with an application operation. Buffering is done to cope with a speed mismatch between the producer and consumer of a data stream or to adapt between devices that have different data transfer sizes.
    - **Caching :** Kernel maintains cache memory which is region of fast memory that holds copies of data. Access to the cached copy is more efficient to that of original.
    - **Spooling and Device Reservation :** A spool is a buffer that holds output for a device, such as printer, that cannot accept interleaved data streams. The spooling system copies the queued spool files to the printer one at a time. In some operating systems, spooling is managed by a system daemon process. In other operating systems, it is handled by an in kernel thread.
    - **Error Handling :** An OS that uses protected memory can guard against many kinds of hardware and application errors.

---

### Physical Organization of CD-ROM

- **Compact Disk -** read only memory (write once)
- Data is encoded and read optically with a laser
- Can store around 600MB of data
    
    ---
    
- Digital data is represented as a series of Pits and Lands :
- **Pit :** a little depression, forming a lower level in the track
- **Land :** the flat part between pits, or the upper levels in the track.
    
    ---
    

**Organization of Data** 

- Reading a CD is done by shining a laser at the discand detecting changing reflections patterns.
    
    1 = change in height (land to pit or pit to land)
    
    0 = a “fixed” amount of time between 1’s
    
    - Representation of Pit and Land ➖
        
        ![disc.PNG](Unit%206%20I%20O%20Management%20&%20Deadlock/disc.png)
        

---

## Deadlocks

- A **deadlock** happens in operating system when two or more processes need some resource to complete their execution that is held by other process.

### Coffman Conditions

- A deadlock occurs if the four Coffman conditions hold true. But these conditions are not mutually exclusive.
- The Coffman Conditions are given below ➖
- **Mutual Exclusion :** There should be a resource that can only be held by one process at a time.
- **Hold and Wait :** A process can hold multiple resources and still request more resources from other processes which are holding them.
- **No Preemption :** A resource cannot be preempted from a process by force. A process can only release a resource voluntarily.
- **Circular Wait :** A process is waiting for the resource held by the second process, which is waiting for the resource held by the third process and so on, till the last process is waiting for resource held by the first process. This forms a circular chain.
    
    ---
    
- **Deadlock Detection :** A deadlock can be detected by a resource scheduler as it keeps track of all the resources that are allocated to different processes. After a deadlock is detected, it can be resolved using the following methods :
    - All the processes involved in the deadlock are terminated. This is not a good approach as all the progress made by the processes is destroyed.
    - Resources can be preempted from some processes and given to others till the deadlock is resolved.
- **Deadlock Prevention :** It is very important to prevent a deadlock before it can occur. So, the system checks each transaction before it is executed to make sure it does not lead to deadlock. If there is even a slight chance that a transaction may lead to deadlock in the future, it is never allowed to execute.
- **Deadlock Avoidance :** It is better to avoid a deadlock rather than take measures after the deadlock has occurred. The wait for graph can be used for deadlock avoidance. This is however only useful for smaller databases as it can quite complex in larger databases.