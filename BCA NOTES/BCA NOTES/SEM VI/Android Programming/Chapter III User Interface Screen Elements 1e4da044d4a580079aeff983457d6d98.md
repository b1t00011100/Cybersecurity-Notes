# Chapter III : User Interface Screen Elements

### Toast & Snack Bar

- **Toast -**
- **Android Toast** is used to display information for the short period of time.
- A toast contains message to be displayed quickly and disappear after sometime.
- *android.widget.Toast* class is the subclass of *java.lang.Object* class
- User can create custom toast to display the images with the text.
- How to create the **Toast :**
    
    ```java
    Toast toast = Toast.makeText(getApplicationContext(),"Hello ",Toast.LENGTH_SHORT);
    ```
    
- There are only 2 constants of Toast class :
    
    
    | Constant | Description |
    | --- | --- |
    | public static final int LENGTH_LONG | Displays view for the long duration of time |
    | public static final int LENGTH_SHORT | Displays view for the short duration of time. |
- Method of Toast class :
    
    
    | Method | Description |
    | --- | --- |
    | public static Toast makeText(Context context, CharSequence text, int duration | makes the toast containing text and duration |
    | public void show() | displays toast |
    | public void setMargin (float horizontalMargin, float VerticalMargin) | Changes the horizontal and vertical margin difference |
- **Snackbar -**
- Snack Bar in android is a new widget introduced with the Material Design library as a replacement of a Toast.
- It is used to show the messages in the bottom of the application with swiping enabled.
- It contain option action button.
- Difference : -
    
    
    | **Snackbar** | **Toast** |
    | --- | --- |
    | Snackbar can be only showed in the bottom of the screen | A Toast message can be customized and printed anywhere  on the screen |
    | Snackbar may have action button optionally | A toast message doesn’t have a action button |
    | Snackbar can be swiped off before the time limit | Toast message cannot be off until the time limit finish |
- Toast message and Snackbar have display length property in common.
- How to create Snackbar :
    
    ```java
    Snackbar snackbar = Snackbar.make(coordinatorLayout, "www.example.com", Snackbar.LENGTH_LONG);
    snackbar.show()
    ```
    

### Custom Toast

- Sometimes displaying the text on Toast may not be satisfactory
- So we can extend the functionalities of toast by creating custom toast.
- Steps for Implementation of Custom Toast :
    - Step I - In first step Retrieve the Layout Inflater with *getLayoutInflater()* (or *getSystemService())* and then inflate the layout from XML using inflate*(int, ViewGroup*). In inflate method first parameter is the layout resource ID and the second is the root View.
    - Step II - Create a new Toast with Toast(Context) and set some properties of the Toast, such as the duration and gravity.
    - Step III - Call *setView(View)* and pass the inflated layout in this method.
    - Step IV - Display the Toast on the screen using show() method of Toast

### Button

- A **Button** is a widget which can be pressed or clicked, by the user to perform some action.
- Android buttons are GUI components which are sensible to taps by the user.
- When the user clicks on button in an Android app, the app responds to the clicks by executing suitable code written in the function onClick.
- There are different types of buttons used in android such as **CompoundButton**, **ToggleButton**, **RadioButton**.
- Some of the button attributes :
    
    
    | Sr.No | Name | Description |
    | --- | --- | --- |
    | 1 | android:background | This is a drawable to use as the background |
    | 2 | android:contentDescription | This defines text that briefly describes content of the view |
    | 3 | android:id | This supplies an identifier name for this view |
    | 4 | android:onClick | This is the name of the method in this View’s context to invoke when the view is clicked |
    | 5 | android:visibility | This controls the initial visibility of the view |
- **Toggle Button**
    - **Android Toggle Button** can be used to display checked/unchecked state on the button.
    - It can be used to On/Off sound, Wifi, Bluetooth, etc
    - Android 4.0, there is another type of toggle button called *switch* that provides slider control
    - Toggle Button Attributes
        
        
        | Name | Description |
        | --- | --- |
        | android:disabledAlpha | The alpha to apply to the indicator when disabled |
        | android:textOff | The text for the button when it is not checked |
        | android:textOn | The text for the button when it is checked |
- **Switch Button**
    - Switch is a two-state user interface element which is used to display ON or OFF states as a button with thumb slider.
    - By using thumb, the user may drag back and forth to choose an option either ON or OFF.
    - It is used to change the setting between two states wither ON or OFF.
    - By default, the android Switch will be in OFF (Unchecked) state. We can change the default state of Switch by using android:checked attribute
    - Switch Button Attributes :
        
        
        | Name | Description |
        | --- | --- |
        | android:id | It is used to uniquely identify the control |
        | android:checked | It is used to specify the current state of switch control |
        | android:gravity | It is used to specify how to align the text like left, right, center, top etc |
- **Image Button**
    - In Android, you can display a normal “Button”, with a customized image background.
    - Image Button is a button with an image that can be pressed or clicked by the users.
    - It looks like a normal button with the standard button background that changes the color during different button states.
    - An image on the surface of a button is defined within an xml by using src attribute or within java class by using setImageResource() method.
    - ImageButton has all the properties of a normal button so you can easily perform any event like click or any other which you can perform on normal button.
    
- **Radio Button**
    - RadioButton is a two states button which is either checked or unchecked.
    - Clicking an unchecked button changes its state to “checked” state and ”unchecked”for the previously selected radio button.
    - If RadioButtons are in group, when one RadioButton within a group is selected, all others are automatically deselected

### **TextView, EditText and CheckBox**

- A **TextView** is a component used to display text to the user.
- TextView attributes from the Textbook!!
- **EditText** is used in applications in order to provide an input or text field, especially in forms.
- It is an overlay over TextView that configures itself to be editable.
- Android EditText is a subclass of TextView.
- EditText view also from textbook!!
- **Android CheckBox** is a type of two state button either checked or unchecked.
- You should use check-boxes when presenting users with a group of selectable options that are not mutually exclusive.
- For example, it can be used to know the hobby of the user, activate/deactivate the specific action.
- Attributes from textbook!

### Alert Dialog and Bottom Sheets

- **Android AlertDialog** is used to display the dialog message with OK and Cancel buttons.
- It is used to interrupt and ask the user about his/her choice to continue or discontinue.
- Android AlertDialog is composed of three regions: title, content area and action buttons.
- It is a subclass of Dialog class.
- Android Alert Dialog is built with the use of three fields: Title, Message area, Action Button. Alert Dialog code has three methods :
    - setTitle() method for displaying the Alert Dialog box Title.
    - setMessage() method used for displaying the message
    - setIcon() method is used to set the icon on Alert Dialog box
- **Android Bottom Sheet** components slides up from bottom showing more relevant content.
- Bottom Sheet is a really nice way to create improved UI and UX designs.
- They are used by almost all big applications like Uber, Google Maps, Google Docs, and almost any other google applications.
- Android comes with built in support for making bottom sheets.
- There are two major types of bottom sheets :
    - **Persistent bottom sheet :** Normally used to display additional information to that shown in the main view. These panels have the same elevation as the main content and remain visible even when not being actively used.
    - **Modal bottom sheet :** Commonly used as an alternative to simple menus or dialogs. They have a higher elevation than the main content, darken the display, and it is necessary to hide them continue to interact with the rest of the application.

### Spinner

- It is used to display the multiple options to the user in which only one item can be selected by the user.
- Android spinner is like the drop down menu with multiple values from which the user can select only one value
- Android spinner is associated with AdapterView. So you need to use one of the adapter classes with spinner.

### Date Picker and Time Picker

- They are used to display date and time selection widget, in android application
- They can be used in either spinner mode or calendar mod (date picker), clock mode (time picker).
- User can control their appearance with their properties.
- Some of the attributes of Date picker and Time picker
    
    
    | **Name** | **Description** |
    | --- | --- |
    | datePickerMode | Value can be spinner or calendar. Both will let you choose date. |
    | calendarViewShown | This is a boolean value, only takes effect when datePickerMode is spinner. If set to true, it will display a calendar. |
    | spinnerShown | just like above just it will display a spinner |
    | minDate | minimum date in mm/dd/yyyy |
    | maxDate | maximum date in mm//dd/yyyy |
    | startYear | set optional start year |
    | endYear | set optional end year |
- some attributes of Time Picker
    
    
    | **Name** | **Description** |
    | --- | --- |
    | timePickerMode() | Value can be spinner or clock. When its set to clock, it will display clock and when set to spinner it will display spinner |
    | headerBackground | This is a color or drawable resource id which can be set to Time Picker’s header background |
    | is24HourView() | check whether the clock is in 24 hour format |
    | setIs24HourView(boolean 24 Hour View) | Set if use 24 hour time system |
    | getHour() | Get current hour integer value |
    | getMinute() | Get current minute integer value |
    | setOnTimeChangedListener() | set call back listener when time is changed |

### Rating Bar and Progress Bar

- **Rating Bar** is used to get the rating from the app user
- A user can simple touch, drag or click on the stars to set the rating value. The value of rating always returns a floating point number which may be 1.0, 2.5,4.5 etc.
- **Progress Bar** is used to display the status of work being done like analyzing status of work or downloading a file etc
- In Android, by default a progress bar will be displayed as a spinning wheel but if user want it to be displayed as a horizontal bar then you can use style attribute horizontal.

### File Download

- There are many ways to download files. Below are the most common way :
    - User AsyncTask and show the download progress in a dialog.
    - This method will allow you to execute some background processes and update the UI at the same time.