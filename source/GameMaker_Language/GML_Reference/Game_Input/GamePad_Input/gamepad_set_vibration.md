# gamepad_set_vibration

With this function you can set the vibration of the gamepad motors, with
either motor using a value from 0 (no vibration) to 1 (full vibration).
Note that there is no time limit on this function, so you will need to
use a variable or an alarm to switch off the vibration (set motors to 0)
after a given time has passed otherwise the gamepad will continue to
vibrate indefinitely. **NOTE** : This function is currently only
available for the standard **Windows** , **PS4** and **Xbox One** target
modules.

#### Syntax:

``` gml
gamepad_set_vibration(device, left_motor, right_motor);
```

|             |                                                                         |                                                           |
|-------------|-------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument    | Type                                                                    | Description                                               |
| device      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad device "slot" to check.                     |
| left_motor  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The amount of vibration from the left motor from 0 to 1.  |
| right_motor |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The amount of vibration from the right motor from 0 to 1. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if lives = 0
{
    gamepad_set_vibration(0, 1, 1);
    alarm[0] = room_speed / 2;
}
```

The above code would be used (for example) in a collision event to make
the gamepad plugged into "slot" 0 vibrate for half a second, with the
alarm that is set being used to switch it off again once that time has
passed.
