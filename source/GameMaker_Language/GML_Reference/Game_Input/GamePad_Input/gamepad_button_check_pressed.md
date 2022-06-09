# gamepad_button_check_pressed

This function will return true or false depending on whether the given
gamepad button is detected as having been pressed or not. Note that this
function will only trigger *once* for the button the first time it is
pressed. For it to trigger again the button must first be released and
then re-pressed. If you need to check a continuous press of the button
you should be using the function [ gamepad_button_check()
](gamepad_button_check) . If you are checking an analogue button,
then the check will take into consideration the [threshold
setting](gamepad_set_button_threshold) and only return true when the
raw input value goes over the given threshold (you can get this raw
value using the function
[gamepad_button_value()](gamepad_button_value) ).

#### Syntax:

``` gml
gamepad_button_check_pressed(device, button);
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
if gamepad_button_check_pressed(0, gp_start)
{
    audio_play_sound(snd_Start, 0, false);
    room_goto(rm_Level_1);
}
```

The above code will detect whether the "start" button of the gamepad
connected to device "slot" 0 has been pressed or not and change room if
it has.
