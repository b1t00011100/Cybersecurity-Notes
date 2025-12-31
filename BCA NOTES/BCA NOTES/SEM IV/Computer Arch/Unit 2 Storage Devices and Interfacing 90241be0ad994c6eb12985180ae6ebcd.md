# Unit 2 : Storage Devices and Interfacing

### Three most common encoding methods :

1. **FM encoding method**
2. **MFM encoding method**
3. **RLL encoding method**

### FM Encoding Scheme

- FM or Frequency Modulation was the original data-encoding scheme used for storing the data on the magnetic recording surface.
- This method of data encoding is also known as “Single density recording”.
- In this method, a clock signal is put with every data signal on the recording surface.
- This clock signal is used for synchronizing the read operation, as there will always be a clock signal, whether the data signal is there or not.
- In this FM method of data recording a 1 bit is stored as two pulses (one clock pulse and one data pulse) and 0 bits stored as a one pulse and one gap or no pulse.
- For example , a binary number 1011 will be stored as PP PN PPPP.

### MFM encoding scheme

- **MFM or Modified frequency modulation.**
- More data can be stored on the same surface or the data storage density can be increased, if the number of pulses required to store the data can be minimized.
- When minimizing the pulses, one should be careful that the number of no pulses together should not be very long; otherwise the disk controller may go out of synchronization with the data.
- The MFM method of data storage, by reducing the number of pulses, is able to store more data without any data and synchronization number of pulses, is able to store more data without any data and synchronization loss. In MFM recording the 0s and 1s are encoded as given below
    - 1 is always stored as no pulse, and a pulse(NP).
    - 0, when preceded by another 0, is stored as a pulse and no pulse (NP).
    - 0, when preceded by a 1, is stored as two no pulses(NN).
    - if you store 1001, on the disk surface using the MFM storage method would be stored as NP NNNP NP.

### RLL encoding scheme

- The RLL is encoding or the  run length limited encoding is the most common encoding scheme used in the harddisk storage.
- This encoding scheme can be accurately called as 2,7 RLL encoding because in this scheme in a series or in a running length the minimum number of 0s next to each other is two and the maximum number of 0s together cannot be more than seven.
- The RLL encoding scheme can store 50 percent more information than MFM encoding scheme on a given surface and it can store three times as much information as FM encoding scheme. The Run Length Limited name comes from the minimum number and maximum number of “no pulse” values allowed between two pulses.
- For the RLL encoding, an encoder/decoder (Endec) table is used to find the pulse signal to be used for different data bit groups . Endec table used by the IBM to convert bit information to the pulse signal is shown below.

| Data Bit | Pulse encoding |
| --- | --- |
| 10 | NPNN |
| 11 | PNNN |
| 000 | NNNPNN |
| 010 | PNNPNN |
| 011 | NNPNNN |
| 0010 | NNPNNPNN |
| 0011 | NNNNPNNN |

---

### Perpendicular encoding

![Perpendicular Encoding.PNG](Unit%202%20Storage%20Devices%20and%20Interfacing/Perpendicular_Encoding.png)

- Perpendicular recording is a technology for data recording on magnetic media, particularly hard disks.
- Perpendicular recording can deliver more than three times the storage density of traditional longitudinal recording.
- In 1986, Maxell announced a floppy disk using perpendicular recording that could store 100kB per inch (38 kB/cm).
- Perpendicular recording was later used by Toshiba in 3”5 floppy disks in 1989 to permit 2.88 MB of capacity, but they failed to succeed in the marketplace.

---

### Hard Disk Construction & Working

![hardisk.PNG](Unit%202%20Storage%20Devices%20and%20Interfacing/hardisk.png)

- A hard disk drive is made up of several physical components
1. Disk platters
2. Read/write heads
3. Head actuator mechanism
4. Spindle motor
5. Logic board
6. Cables and connectors
7. Bezel / Front Plate
8. Air Filter
- **Hard Disk Platters :**
    - The platters stores information. It comes in varying sizes like 5.12”, 3.14”, etc.
    - The physical size of a drive is expressed as the size of the platters
    - Most hard disks have two or more platters
    - Platters were originally made from an **Aluminium**/magnesium alloy which provides both strength and lightweight
    - All modern drives use glass or glass ceramic plates.
- **Read/Write Heads :**
    - A harddisk drive usually has one read/write head for each platter surface (meaning that each platter has two sets of read/write heads-one for topside and one for bottom).
    - These heads are connected on a single movement mechanism so heads across the platters in unison.
    - The HDD uses various types of heads for read/write purpose
        - Ferrite head
        - Metal-In-Gap Head, Thin Film Head
        - Magneto Resistive Head
        - Giant Magneto Resistive Head
- **Head Actuator Mechanism**
    - This mechanism moves the heads across the disk and positions them accurately above the desired cylinder.
    - Two basic categories are used
        - Stepper Motor Mechanism
        - Voice Coil Actuator
    - Stepper Motor actuators were commonly used on hard drives made during the 1980s and early 1990s with capacities of 100MB or less
    - Floppy disk drives position their heads by using a Stepper motor actuator
    - All hard disks drives being manufactures today used voice coil actuator.
- **Voice Coil Actuator**
    - The two main types of voice coil positioner mechanism are
        - **Linear Voice Coil Actuators**
        - **Rotary Voice Actuator**
- **Spindle Motor**
    - The spindle motor spins the platters connected to spindle. The motor is directly connected to the spindle of platters. These platters revolve at exactly 3600 rpm to 1500 rpm. The speed of motor has to be controlled very precisely.
    - Normally a feedback loop is employed in the control electronics to monitor the speed. The speed control is fully automatic.
- **Logic Boards**
    - A disk drive will have a board containing the electronics that control the drive’s spindle and head actuator systems These are called logic boards.
    - They present data to the controller in a planned format
    - They may be removed and replaced to rectify a logic board problem.
- **Cable and Connectors**
    - Cable and connectors are used to connect HDD to the main computer systems.
    - All hard disks drive contains connections for data/control interface connectors, Power connector.
- **Bezel /Front Faceplate**
    - Bezel is the front faceplate provided on most of the hard disk drives.

### Terms Related to Hard disk

![diaghdd.PNG](Unit%202%20Storage%20Devices%20and%20Interfacing/diaghdd.png)

- When OS writes some information on the harddisk, it does not allocate the space sector wise, instead uses a new storage called “Cluster”.
- Clusters are the minimum space allocated by the DOS when storing any information on the disk
- Even to store only one byte long information on the disk requires minimum one cluster area on the disk surface.
- A cluster can be made up of one or more sectors , it depends on disk type being used.
- This reduces the size of the FAT that DOS uses to keep track of the used and empty disk spaces.
- First Cluster no is taken as 2
- Clusters are used to allocate the storage area for data area only, FAT and directory are as are not allocated according to the cluster size.
- **Cylinder :** Same tracks of different platters from an imaginary cylinder like structure Data is stored cylinder by cylinder.
    - All tracks on a cylinder are written and then the R/W head moves to the next cylinder.
    - This reduces movement of R/W head and increases the speed of read and write operation.
- **Sector :** A track is a big area to store data (5000 bytes). Hence tracks are divided into sector.
    - The formatting program divides disk surface into sectors by writing magnetic pattern on disk surface.
    - Different HDD capacities have different number of tracks.
    - 512 byte data can be stored in each sector. Sector no starts from 1.
- **Landing zone :** This setting specifies the cylinder to which the BIOS should send the heads of the hard disk when the machine is to be turned off. This is where the heads will "land" when they spin down. Modern drives automatically park the heads in a special area that contains no data when the power is turned off. Therefore this setting is meaningless and is typically ignored.
    - Most BIOS set this value to be the largest cylinder number of the logical geometry specified for the disk when auto detection takes place. So if the drive has 6,136 logical cylinders, the landing zone will be set to 6,135. In any event a modern IDE drive will ignore this setting and auto-park by itself.
- **Zone Recording :** One way to increase the capacity of a hard drive during the low level format is to create more sectors on the disks Outer cylinders than on the inner ones.
    - Because they have a larger circumference the outer cylinders can hold more data .Drives that
    use zoned recording split the cylinders into groups called zones, with each successive
    zone having more sectors per track as you move outward from the center of disk