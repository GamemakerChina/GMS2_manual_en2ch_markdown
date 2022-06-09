# gamepad_set_option

This function can be used to set any of the available gamepad options.
You supply the gamepad "slot" to set the option on, as well as the
option string to set and the value to use. The available option string
will depend on the platform that the project is being run on, as listed
below:

|                  |          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |         |
|------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| Option           | Platform | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Value   |
| "allow_rotation" | tvOS     | Set whether the Siri Remote will be rotation locked (ie: can only be used vertically) or not. When unlocked (a value of true ) rotating the control will change the input, such that a rotation of 90º to the left will make the "right" side of the touch pad return "up", etc... such that all input will be relative to the orientation of the device. When locked (a value of false ) then the input will not be changed relative to the position of the controller and will always be treated as if the controller is in a vertical position.     | Boolean |
| "dpad_absolute"  | tvOS     | Set whether the Siri Remote touchpad accepts absolute input, or relative input. In absolute mode (a value of true ) the center of the touch pad is considered the (0,0) position - ie: where the analog stick is at rest or where the center of the dpad would be - and movement around this position will generate input. When set to relative (a value of false then the (0,0) position will be considered as being wherever the initial touch on the pad is made and all input will be generated from that position, not the center of the pad.     | Boolean |

#### Syntax:

``` gml
gamepad_set_option(device, option_name, value);
```

|             |                                                                                                                                                                                                                                     |                                                                                       |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Argument    | Type                                                                                                                                                                                                                                | Description                                                                           |
| device      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                                              | Which gamepad device "slot" to set.                                                   |
| option_name |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                                            | The name of the option to set (a string, see the table above)                         |
| value       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types) , [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types) , or [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)      | The value to set the option to (can be boolean, real or string - see the table above) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; 12; ++i;)
{
    if gamepad_is_connected(i) &amp;amp;&amp;amp; gamepad_get_description(i) == "tvOS Siri Remote"
    {
        if gamepad_get_option(i, "allow_rotation") == false
        {
            gamepad_set_option(i, "allow_rotation", true);
        }
    }
}
```

The above code loops through all the gamepad slots and checks for the
"Siri Remote" on the tvOS platform. If one is detected, it then sets the
remote to allow input rotation.
