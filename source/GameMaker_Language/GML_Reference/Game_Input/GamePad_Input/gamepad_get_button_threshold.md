# gamepad_get_button_threshold

This function can be used to detect the current threshold setting of the
analogue buttons for a given device. The default threshold for all
analogue buttons is 0.5, with the range being from 0 to 1. The threshold
defines at what point the button is considered as being "pressed" for
games that require them to act as a digital button.

#### Syntax:

``` gml
gamepad_get_button_threshold(device);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad device "slot" to check. |

#### Returns:

``` gml
 Real
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
