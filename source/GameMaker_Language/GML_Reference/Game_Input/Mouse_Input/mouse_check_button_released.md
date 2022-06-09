# mouse_check_button_released

This function will return true if the mouse button being checked has
been released or false if it has not. This function will only be
triggered *once* for any mouse button when it is released and to trigger
it again the button will need to have been pressed and released again.
You supply the mouse button to check from one of the following
constants:

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
mouse_check_button_released(numb);
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
if mouse_check_button_released(mb_right)
{
    speed = point_distance(x, y, mouse_x, mouse_y) / 10;
}
```

The above code will check to see if the right mouse button has been
released and if it has it will set the speed of the instance to a tenth
of the distance between the current x/y position and the mouse x/y
position.
