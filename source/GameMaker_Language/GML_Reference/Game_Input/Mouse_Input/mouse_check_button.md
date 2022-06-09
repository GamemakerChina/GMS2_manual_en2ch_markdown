# mouse_check_button

This function will return true if the mouse button being checked is held
down or false if it is not. You supply the mouse button to check from
one of the following constants:

|                                                                                                                          |                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
|  [Mouse Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/mouse_check_button)  |                                                                          |
| Constant                                                                                                                 | Description                                                              |
| mb_left                                                                                                                  | The left mouse button                                                    |
| mb_middle                                                                                                                | The middle mouse button (this may not be valid for all target platforms) |
| mb_right                                                                                                                 | The right mouse button                                                   |
| mb_side1 \*                                                                                                              | Mouse side button 1                                                      |
| mb_side2 \*                                                                                                              | Mouse side button 2                                                      |
| mb_any                                                                                                                   | Any of the mouse buttons                                                 |
| mb_none                                                                                                                  | No mouse button                                                          |

\* **NOTE** : The **mb_side1** and **mb_side2** buttons are only for use
on Windows, macOS, Ubuntu and HTML5.

#### Syntax:

``` gml
mouse_check_button(numb);
```

|          |                                                                                                                          |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                     | Description                               |
| numb     |  [Mouse Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/mouse_check_button)  | Which mouse button constant to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mouse_check_button(mb_left)
{
    instance_create_layer(mouse_x, mouse_y, "Effects", obj_Star);
}
```

The above code will check for the left mouse button and every step that
it is held down will create an instance of the object indexed in
"obj_Star".
