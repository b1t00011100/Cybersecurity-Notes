# Unit V : Android User Interface Elements

### Layouts

- An Android Layout is a class that is responsible for arranging the way its children appears on the screen.
- Anything that is a View or which is inherit from the view can be a child of a layout. All of the layouts in android are inherited from **ViewGroup** (which inherits from the view).
- Android allows you to create view layouts using simple XML file.
- **Linear Layout**
    - It is the simplest layout used in android for layout designing.
    - Linear Layout displays all the elements in linear fashion means all the childs/elements of a linear layout are displayed according to its orientation.
    - The value for orientation property can be either horizontal or vertical.
- **Absolute Layout**
    - An Absolute Layout is a layout used to design the custom layouts.
    - In this layout the exact location of its children by using X and Y coordinates can be specify.
        
        <aside>
        💡
        
        **Absolute layout** are harder to preserve for different mobile screen sizes than other
        types of layouts because we set the exact location of a child view or called component. The positioning is based on x(top) and y(left) coordinates and that positioning is not as useful in world of various screen resolutions(sizes) and aspect ratios.
        
        </aside>
        
- **Frame Layout**
    - Frame Layout is a layout which is designed to block out an area on the screen to display a single item.
    - The frame layout is often used as a container layout, as it generally only has a single child view.
    - Multiple children to a FrameLayout can be added and control their position by assigning gravity to each child, using the *android:layout_gravity* attribute.
- **Relative Layout**
    - Relative Layout is layout which lets you position your component base on the nearby component’s position.
    - It’s the most flexible layout that allows you to position your component to display in anywhere you want.
    - In Relative Layout, one can use “above, below, left and right” to arrange the component’s position in relation to other component.
- **Table Layout**
    - Table Layout is a layout which is used to arrange the group of views into rows and columns.
    - The container of table layout do not display a border line for their columns, rows or cells.
    - A table will have many columns and rows with the most cells.
    - A table can also leave the cells empty but cells can’t span the columns as they can in HTML.
- **Creation of Layout Programmatically -**
    - In some cases, you have to create and style a Linear Layout, Relative Layout or any other layout programmatically.
    - Atrributes that you can programmatically apply to the layout can be background color, layout width, height, margins, orientation, layout gravity, paddings and so on.
    - Linear Layout class is used to create Linear Layout.
    
    ```jsx
    LinearLayout layout = new LinearLayout(MainActivity.this);
    ```
    
    - rest pretty technical code stuff look through textbook!

### View