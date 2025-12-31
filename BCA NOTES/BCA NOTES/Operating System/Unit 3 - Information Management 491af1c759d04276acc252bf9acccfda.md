# Unit 3 - Information Management

### Introduction

- Operating system can be measured to be a collection of various callable programs or services.
    - These services can be categorized by three heads.
        1. Information Management
        2. Process Management
        3. Memory Management
- **Information Management -** is the collection and management of information from one or more sources and the allocation of that information to one or more addresses.
- Operating system manages the information or data, or managing the information from which it should be sent or received. File system in OS keeps the track of information, its location and everything.
    - It also decides on which user should get resources first and put into effect the protection requirements and also provides accessing routines.
    - Some of the system calls in this category are :-
        
        
        | Create a file |
        | --- |
        | Create a directory |
        | Open a file |
        | Close a file |
        | Read data from file to buffer |
        | Write data from buffer to life |
        | Move the file pointer |
        | Read and return a file’s status |
        | Create a pipe |
        | Create a link |
        | Change working directory |

---

### Information Maintenance

- Many system calls exist simply for the purpose of transferring information between the user program and OS.
    - For example, most systems have a system call to return the time and date.
- In addition, the operating system keeps information about all its processes, and system calls are used to access this information.
- Other system calls :- number of current users, version no of the OS, amount of free memory or disk space.

---

### Disk Basics

- Alternatively known as **floppy disk**, a disk is a hard or floppy round, flat and magnetic platter capable of having information read from and written to it. The most frequently found disks with a computer are the hard disks and floppy disks.
- Disk is a very important I/O intermediate used by OS.
- The operating principle of a floppy disk is similar to that of hard disk, And a hard disk can be considered as being made of multiple floppy disks put one above the other.
- **Working of disk** : Disk is nothing but long play music records except that the recording is done in concentric circles and not by spirally. A Floppy disk is made up of a round piece of plastic material,
coated with a magnetized recording material. The surface is made up of concentric circles which are called as tracks. Data is recorded on these tracks in bit and it contains magnetized particles of metal is having north and South Pole. It is having only two directions so each particle can acts as a binary values of 0 or 1 and 8 switches can record a character with the coding methods (ASCII). A logical record which consists of different fields (data items), each consisting of several characters which is stored in floppy disk

---

### Optical Disks

- Optical disks record data by burning microscopic holes in the surface of the disk with a laser. To read the disk, another laser beam shines on the disk and detects the holes by changes in  the reflection pattern.
- Optical disks come in three basic forms
    - **CD-ROM :** Most optical disks are read-only. When you purchase them, they are already filled with data. You cannot modify, delete or write new data.
    - **WORM :** Stands for write-once, read-many