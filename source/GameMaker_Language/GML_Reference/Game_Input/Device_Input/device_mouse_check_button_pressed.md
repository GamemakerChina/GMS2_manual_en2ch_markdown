# device_mouse_check_button_pressed

This function returns true or false depending on whether the device that
you specify has been "touched" (clicked) or not. The device argument
refers to the touch number, which can be from 0 to n and the maximum
number of touches that can be detected will depend very much on the
device being used and the OS it runs (most devices will support at least
4 simultaneous touches). This function is only triggered *once* by the
actual pressing action, and the constants listed [on this
page](../Mouse_Input/Mouse_Input) can be used to check for the mouse
buttons. Note that mb_right will only be detected if a double tap touch
is detected and held on the second tap (this behavior can be disabled
using the function
[device_mouse_dbclick_enable()](device_mouse_dbclick_enable) ).

#### Syntax:

``` gml
device_mouse_check_button_pressed(device, button);
```

|          |                                                                                                                          |                                                   |
|----------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                                                                     | Description                                       |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The device (from 0 - *n* ) that is being checked. |
| button   |  [Mouse Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/mouse_check_button)  | The button of the device that is being checked.   |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if device_mouse_check_button_pressed(0, mb_left)
{
    press = true;
}
```

The above code checks to see if the device has been pressed and sets a
variable to true if it has.
