# gamepad_button_check_released

This function will return true or false depending on whether the given
gamepad button is detected as having been released or not. Note that
this function will only trigger *once* for the button the moment it has
been released. For it to trigger again the button must first be pressed
and then released once more. If you are checking an analogue button,
then the check will take into consideration the [threshold
setting](gamepad_set_button_threshold) and only return true when the
raw input value goes under the given threshold (you can get this raw
value using the function
[gamepad_button_value()](gamepad_button_value) ).

#### Syntax:

``` gml
gamepad_button_check_released(device, button);
```

|          |                                                                                                                              |                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                                         | Description                                                      |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | Which gamepad device "slot" to check.                            |
| button   |  [Gamepad Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/GamePad_Input/gamepad_axis_value)  | Which gamepad button [constant](Gamepad_Input) to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gamepad_button_check_released(0, gp_select)
{
    audio_play_sound(snd_Button, 0, false);
    global.Pause = !global.Pause;
}
```

The above code will detect whether the "select" button of the gamepad
connected to device "slot" 0 has been pressed or not and toggle the
global "Pause" variable.
