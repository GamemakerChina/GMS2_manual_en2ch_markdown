# gamepad_is_connected

This function will return whether a gamepad is connected to the given
"slot" (returns true ) or not (returns false ). You would normally use
this function in conjunction with the [ gamepad_get_device_count()
](gamepad_get_device_count) function to get the correct number of
available game pads and/or gamepad "slots". Note that there may be a
slight delay between the user connecting the gamepad and GameMaker
detecting it as being connected (this is especially the case when
dealing with bluetooth connected controllers). **NOTE** : On some
platfroms - especially consoles - this function may return false
immediately after a gamepad has been connected/selected and may need to
be checked in an alarm a few frames (steps) later for it to correctly
detect the gamepad.

#### Syntax:

``` gml
gamepad_is_connected(numb);
```

|          |                                                                         |                                |
|----------|-------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                    | Description                    |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad "slot" to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var gp_num = gamepad_get_device_count();
for (var i = 0; i &amp;lt; gp_num; i++;)
{
    if gamepad_is_connected(i) global.gp[i] = true else global.gp[i] = false;
}
```

The above code loops through the available game pads (or gamepad slots)
and then checks each one for a connected gamepad. the returned value is
then used to set a global array to true or false for use in future
checks.
