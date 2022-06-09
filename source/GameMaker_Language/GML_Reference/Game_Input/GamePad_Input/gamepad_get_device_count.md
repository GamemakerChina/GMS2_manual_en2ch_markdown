# gamepad_get_device_count

This function will tell you one of two things. Either the number of game
pads connected, *or* the number of available "slots" for game pads to be
connected to. The actual return value will depend on the platform and
the internal configuration of that platform and as such this function
should be used in conjunction with the function [ gamepad_is_connected()
](gamepad_is_connected) to make sure of the exact number of pads
connected at any time.

#### Syntax:

``` gml
gamepad_get_device_count();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var gp_num = gamepad_get_device_count();
for (var i = 0; i &amp;lt; gp_num; i++;)
{
    if gamepad_is_connected(i)
    {
        global.gp[i] = true;
    }
    else
    {
        global.gp[i] = false;
    }
}
```

The above code loops through the available game pads (or gamepad slots)
and then checks each one for a connected gamepad. the returned value is
then used to set a global array to true or false for use in future
checks.
