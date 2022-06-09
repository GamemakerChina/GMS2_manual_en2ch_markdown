# gamepad_button_value

With this function you can get the current value of an analogue button,
from 0 to 1, where 0 is no pressure and 1 is full pressure. You supply
the gamepad slot index to check, along with either a button constant (as
listed [here](Gamepad_Input) ), or an integer value between 0 and [
gamepad_button_count() ](gamepad_button_count) - 1 . Note that this
will return the *raw* value for the button, and does *not* take into
account the setting for the threshold (see
[here](gamepad_set_button_threshold) for more information on
thresholds).

#### Syntax:

``` gml
gamepad_button_value(device, button);
```

|          |                                                                                                                              |                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                                         | Description                                                      |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | Which gamepad device "slot" to check.                            |
| button   |  [Gamepad Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/GamePad_Input/gamepad_axis_value)  | Which gamepad button [constant](Gamepad_Input) to check for. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
speed = gamepad_button_value(0, gp_shoulderrb) * 4;
```

The above code uses the analogue trigger value from the gamepad plugged
into device "slot" 0 to set the speed of the instance.
