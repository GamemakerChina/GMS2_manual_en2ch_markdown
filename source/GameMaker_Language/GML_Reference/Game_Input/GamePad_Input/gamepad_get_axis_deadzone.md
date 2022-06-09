# gamepad_get_axis_deadzone

This function can be used to get the "dead zone" value of the joystick
axis. You specify the device slot to get, and the function will return a
value between 0 to 1, where value reflects the threshold under which the
joystick axis is considered to be at 0.

#### Syntax:

``` gml
gamepad_get_axis_deadzone(device);
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
if gamepad_get_axis_deadzone(global.PadId) != 0.5
{
    gamepad_set_axis_deadzone(global.PadId, 0.5);
}
```

The above code checks the analogue axis threshold of the gamepad
connected to the device "slot" stored in the global variable and if it
is not the default value of 0.5, it is set to that value.
