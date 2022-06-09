# gamepad_set_button_threshold

This function can be used to set the current threshold setting of the
analogue buttons for a given device. The default threshold for all
analogue buttons is 0.5, with the range being from 0 to 1. The threshold
defines at what point the button is considered as being "pressed" for
games that require them to act as a digital button. This function will
affect the [check](gamepad_button_check) ,
[pressed](gamepad_button_check_pressed) and
[released](gamepad_button_check_released) states for analogue
buttons, but will *not* affect the value returned by the function [
gamepad_button_value() ](gamepad_button_value) , which will always
return the raw value for the button.

#### Syntax:

``` gml
gamepad_set_button_threshold(device, threshold);
```

|           |                                                                         |                                                    |
|-----------|-------------------------------------------------------------------------|----------------------------------------------------|
| Argument  | Type                                                                    | Description                                        |
| device    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad device "slot" to check.              |
| threshold |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new threshold value (from 0 - 1, default 0.5). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gamepad_get_button_threshold(0) != 0.5
{
    gamepad_set_button_threshold(0, 0.5);
}
```

The above code checks the analogue button threshold of the gamepad
connected to device "slot" 0 and if it is not the default value of 0.5,
it is set to that value.
