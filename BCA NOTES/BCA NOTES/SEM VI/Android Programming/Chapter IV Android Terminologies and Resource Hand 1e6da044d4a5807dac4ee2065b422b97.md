# Chapter IV : Android Terminologies and Resource Handling

### Terminologies

| **XML** | In Android, XML file is used for designing the application’s user interface like creating layouts, views, buttons, text fields, etc. and it is used in parsing data feeds from the internet |
| --- | --- |
| **View** | A view is an UI which occupies rectangular area on the screen to draw and handle user events. |
| **Layout** | Layout is the parent of view. It organizes all the views in a proper manner on the screen. |
| **Activity** | An activity is a device’s screen which users see and interact. User can place UI elements in any order in the created window of user’s choice. |
| **Emulator** | An emulator is an Android virtual device through which you can select the target Android version or platform to run and test your own developed application |
| **Manifest file** | It is a metadata for every application. This file contains all the essential information about the application like app icon, app name, launcher activity. User can set all the permission like Send SMS, Bluetooth, Camera in this file |
| **Service** | Services are the process which run in the Background. It is not associated with any activity as there is no UI. Any other component of the application can start a service and this service will continue to run even when the user switches from one application to another. |
| **Broadcast Receiver** | Broadcast Receiver is another building block of Android application development which allows you to register for system and application events. It works in such a way that, when the event triggers for the first time all the registered receivers through this broadcast receiver will get notified for all the events by Android Runtime. |
| **Content Providers** | Content Providers are used to share data between two applications. This can be implemented in two ways : 1) When you want to implement the existing content provider in another application. 2) When you want to create new content provider that can share its data with other applications. |
| Intent  | Intent is a message passing mechanism which is used to communicate between two or more components like services, activities, broadcast receiver etc. Intent can also be used to start an activity or service or to deliver broadcast message. |
- **Context -**
    - The Context class gives you access to the global information about an applications environment.
    - It lets you to access the apps resources and classes and communicate with other app components.
    - The context gives you access to the system services. This enables you to interact with the various managers, some examples being the :
        1. AlarmManager
        2. AudioManger
        3. LocationManager
    - Context also helps the current activity to interact with outside android environment like local files, databases, class loaders associated to the environment.
    - Following are the methods to get the context
        1. getApplicationContext()
        2. getContext()
        3. getBaseContext()
- **Activity -**
    - An Android activity is one screen of the Android app’s UI, where user interacts.
    - Android activity is very similar to windows in a desktop environment.
    - Android app may have one or more activities (Screens)
    - The Android App starts by showing the main activity, and from there the app may make it possible to open additional activities.
    - **Activity Life Cycle**
        
        ![androidlifecycke.png](Chapter%20IV%20Android%20Terminologies%20and%20Resource%20Hand/androidlifecycke.png)
        
    - Do Methods From Textbook!!
- **Intent -**
    - Intent is a message passing mechanism which is used to communicate between two or more components like services, activities, broadcast receivers etc. Intent can also be used to start an activity or service or to deliver broadcast messages.
    - Intents are also used to transfer data between activities.
    - Following are the uses of Intent :
        - For Launching an Activity
        - To start a new service
        - For Broadcasting messages
        - To Display a list of contacts in List View
    - Types of Intent
        - **Implicit Intent -** An Implicit intent specifies an action that can invoke any app on the device to be able to perform an action. Using an Implicit Intent is useful when your app cannot perform the certain action but other apps probably can and you‘d like the user to pick which app to use.
            - Some Examples of Implicit intent are Call, Dialpad, Contact, Browser, Call Log, Gallery, Camera.
        - **Explicit Intent -** An explicit intent is an intent where you explicitly define the component that needs to be called by the Android system. An explicit Intent is one that you can use to launch a specific app component, such as a particular activity or service in your app.
    - **Linking Activity using Intent -** An Android application can contain zero or more activities. When your application has more than one activity, you may need to navigate from one activity to another.
    - Steps to Link Activities :
        - Step 1.create new android project.
        - Step 2.add new Activity by right click on package name under src folder then choose New –> Other –> AndroidActivity, And give it a name (Ex. ―Activity2‖) and press finish button.
        - Step 3. After that add newly created activity to AndroidManifest.xml
        - Step 4:Then go to res –> layout –> right click –> New –> Other –> Android XML File … ( Ex. activity_activity2.xml )
        

### Notification Service

- **Services : Services** are part of the application and run on a different thread in the background and supports some long-running operation, such as handling location updates from the Location Manager. services operate outside of the user interface.
- **Notification :** Notification allows apps or services associated with an app to inform the user of an event, Notification on Android can be done in any of the following ways :
    - Status Bar Notification
    - Vibrate
    - Flash Lights
    - Play a sound

### Broadcast

- A *broadcast receiver* is an Android component which allows you to register for system or application events. All registered receivers for an event are notified by the Android runtime once this event happens/triggers.
- For example , applications can register for the ACTION_BOOT_COMPLETED system event which is fired once the Android system has completed the boot process.
- When any of those events occur it brings the application into action by either creating a status bar notification or performing a particular task.

### Adapter Resources

- Adapter is a bridge between an AdapterView and the underlying data for that view.
- It is a View object. This means, you can add it to your activities the same way you add any other user interface widget. However, it is incapable of displaying any data on its own.
- Its contents are always determined by the other object, an adapter.
- **What is a Adapter ?**
    - An Adapter is an object of a class that implements the Adapter Interface. It acts as a link between a data set and a adapter view , an object the extends the abstract AdapterView class.
    - The data set can be anything that presents data in a structured manner like Arrays, Lists, objects, and Cursor objects.
    - An adapter is responsible for retrieving data from a data set and for generating View object based on the data. The generated view objects are then used to populated any adapter view that is bound to the adapter.
    - You can create your own adapter class from scratch, but most developers choose to use or extend adapter classes provided by the Android SDK, such as Array Adapter and SimpleCursorAdapter.
- **How do Adapter Views Work ?**
    - Adapter views can display large data sets very efficiently. For instance, the ListView and GridView widget can display millions of items without any noticeable lag while keeping memory and CPU usage very low.
    - Different adapter views follow different ways. However, here’s what most of them usually do.
    - They render only those view objects that are either already on-screen or that are about to move on-screen. This way, the memory consumed by an adapter view can be constant and independent of the size of the data set.
    - They also allow developers to reduce expensive layout inflate operations and recycle existing View objects that have move off-screen. This keeps CPU consumption low.