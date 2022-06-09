# mouse_check_button_pressed

This function will return true if the mouse button being checked has
been pressed or false if it has not. This function will only be
triggered *once* for any mouse button when it is first pressed and to
trigger it again the button will need to have been released and pressed
again. Note that it will be considered triggered for the duration of the
step, and for all instances that have any mouse events or that use this
same function. You supply the mouse button to check from one of the
following constants:

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
mouse_check_button_pressed(numb);
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
if mouse_check_button_pressed(mb_left)
{
    score += 50;
}
```

The above code will check to see if the left mouse button has been
pressed and if it has it will add 50 to the score.
