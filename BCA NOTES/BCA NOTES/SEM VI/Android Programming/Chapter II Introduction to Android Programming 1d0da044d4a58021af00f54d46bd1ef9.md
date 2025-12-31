# Chapter II : Introduction to Android Programming

### What is Android

- Its an open source operating system based on Linux with a Java programming interface for mobile devices such as Smartphone.
- It was developed by the **Open Handset Alliance (OHA**), which is led by Google. The OHA is a consortium of multiple companies like Samsung, Sony, Intel and many more to provide services and deploy handsets using android platform.
- Unlike IOS Android is Open Source.
- It gives the Opportunity to the Developers to introduce and incorporate any technological advancement.

---

### History and Version

- Android was first created in 2003 by **Andy Rubin** in Palo Alto, Cali.
- He first developed the OS for digital cameras. Soon he realized that the marketplace for digital camera OS wasn’t all that big and Android inc diverted its attention towards smartphones.
- On 17 August 2005, **Google** acquired android Incorporation. Since that time, it is in the subsidiary of Google Incorporation.
- In 2007 **Google** announces the development of android Operating System.
- In 2008, **HTC** launched the first android application.
- Chart of all the Versions :

![android.png](Chapter%20II%20Introduction%20to%20Android%20Programming/android.png)

---

### Android Architecture

![androidarch.png](Chapter%20II%20Introduction%20to%20Android%20Programming/androidarch.png)

- Android OS is roughly divided into five sections and four main layers.
- **Linux Kernel** : At the very bottom of the layer is Linux. This layer provides a level of abstraction between the device hardware and it contains all the essential hardware drivers like camera, keypad, display, etc. The kernel takes care of all the things that Linux is really good at such as networking and a vast array of device drivers..
- **Libraries** : Top of the linux kernel has set of libraries including open-source Web browser engine WebKit, well known library libc, SQLite is a database which is useful repository for storing and sharing of application data, libraries to play and record audio and video, SSL libraries responsible for Internet Security.
- **Android Libraries** : This category includes those Java-based libraries that are specific to Android development. Examples of libraries in this category include the application framework libraries in addition to those that facilitate user interface building, graphics drawing and database access.
- A summary of some key core Android libraries available to the Android developer is as given below −
    - android.app – this provides access to the application model and is the cornerstone of all Android applications.
    - android.content –this Facilitates content access, publishing and messaging between applications and application components.
    - android.database – this access data published by content providers and includes SQLite database management classes.
    - android.opengl – Its Java interface to the OpenGL ES 3D graphics rendering API.
    - android.os – this provides applications with access to standard operating system services including messages, system services and inter-process communication.
    - android.text − Used to render and manipulate text on a device display.
    - android.view − The basic building blocks of application user interfaces
    - android.widget − A rich collection of pre-built user interface components such as buttons, labels, list views, layout managers, radio buttons etc.
    - android.webkit − A set of classes intended to allow web-browsing capabilities to be built into applications.
- **Android Runtime** : This is the third section of the architecture and available on the second layer from the bottom. This section has a very important component called **Dalvik Virtual Machine** which is a kind of Java Virtual Machine specifically designed and optimized for android.
    - The Dalvik VM makes use of linux core features like Memory management and multi-threading, which is fundamental in the Java language. The Dalvik VM enables every Android application to run in its own process, with its own instances of the Dalvik Virtual Machine.
    - The Android runtime also provides a set of core libraries which enable Android developers to write Android applications using standard Java Programming Language.
- **Application Framework** : The Application Framework layer provides many higher-level services to applications in the form of Java classes. Application developer are allowed to make use of these services in their applications. The Android framework includes the following key services —
    - **Activity Manager** : It Controls all aspects of the application lifecycle and activity stack.
    - **Content Providers** : It allows applications to publish and share data with other applications.
    - **Resource Manager** : It provides access to non-code embedded resources such as strings, color settings and user interface layouts.
    - **Notification Manager** : It allows applications to display alerts and notifications to the user.
    - **View System** : this is the set of widgets used to create applications user interfaces.
- **Applications** : This is the top layer of application framework. The application which you create goes on this layer.
Examples. Facebook,google,internet browser, contacts etc.

---

### Dalvik VM

- A virtual machine is same like a software implementation of a physical computer which works like real physical computer. It means virtual machine can compile and run any program just like a physical computer does for us.
- But the dark side of a VM is it is less efficient than a physical computer and provides unstable performance when multiple virtual machines run at the same time on same machine.
- **Dalvik** is a purposely built virtual machine designed specially for android which was developed by **Dan Bornstein** and his team. It was only developed for mobile devices. It uses register based arch. Due to this Dalvik VM has fewer advantages over a JAVA VM such as :
    - Dalvik uses its own 16 bit instruction set while java uses 8 bit stack instructions, which reduce the Dalvik instruction count and raised its interpreter speed.
    - Dalvik uses less space, which means an uncompressed .dex file is smaller in size (few bytes) than compressed java archive file (.jar file).

### Role of Dalvik VM

- In java programming we write and compile java program using java compiler and run that bytecode on the java vm. In android we still write and compile java source file (byte code) on java compiler, and it is once again recompiled using dalvik compiler to dalvik bytecode *(dx tool converts java .class file into .dex format)* and this dalvik bytecode is then executed on the dalvik vm.

---

### Software Stack

- **Android Software Stack** is classified into five different parts:
    1. **Linux based kernel** 
    2. **Native Libraries**
    3. **Android Runtime**
    4. **Application Framework**
    5. **Applications**
- **Terminology**
    - **Android Software Development Kit (Android SDK)** contains the necessary tools to create, compile and package the Android applications.
    - **Android debug bridge (adb),** is a tool that allows you to connect to a virtual or real Android device
    - Google provides two integrated development environments (IDEs) to develop new applications
        - **Application Developer Tools (ADT)** are based on the Eclipse IDE
        - **Android Studio** based on the intelliJ IDE
    - **Android RunTime (ART)** uses Ahead of Time compilation, and optional runtime for Android 4.4
    - **Android Virtual Device (AVD) -** The Android SDK contains an Android device emulator. This emulator can be used to run a Android Virtual Device, which emulates a real Android phone where you can deploy and test your applications.

---

### [R.java](http://R.java) File

- **Android [R.java](http://R.java)** is an auto generated file by *aapt* (Android Asset Packaging Tool) that contains resource IDs for all the resources of res/ directory.
- If you create any component in the activity_main.xml file ex. If u drag a button widget on activity_main.xml file, id for the corresponding component is automatically created in this file. This id can be used in the activity resource file (MainActivity.java) to perform any action on the component.

---

### **Screen Orientation**

- The **ScreenOrientation** is the attribute of activity element. The orientation of android activity can be portrait, landscape, sensor and unspecified etc. it needs to be defined in the AndroidManifest.xml file.  ****

| **Value** | **Description** |
| --- | --- |
| unspecified | It is the default value. In such case, system chooses the orientation |
| portrait | taller not wider |
| landscape | wider not taller |
| sensor | Orientation is determined by the device orientation sensor |

---

### Android Operating System

- Pretty minimal do it from the textbook !!!