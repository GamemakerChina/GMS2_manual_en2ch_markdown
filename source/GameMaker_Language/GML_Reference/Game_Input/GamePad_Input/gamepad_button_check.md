# gamepad_button_check

This function will return true or false depending on whether the given
gamepad button is detected as being held down or not. If you are
checking an analogue button, then the check will take into consideration
the [threshold setting](gamepad_set_button_threshold) and only
return true while the raw input value is over the given threshold (you
can get this raw value using the function
[gamepad_button_value()](gamepad_button_value) ).

#### Syntax:

``` gml
gamepad_button_check(device, button);
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
if gamepad_button_check(0, gp_face1)
{
    if canshoot = true
    {
        audio_play_sound(snd_Shoot, 0, false);
        instance_create_layer(x, y, "Bullets", obj_Bullet)
        canshoot = false;
        alarm[0] = room_speed / 2;
    }
}
```

The above code will detect whether the bottom button of the top face
(the "X" on a ps3 controller) is being held down and if so, it will
shoot a "bullet" instance and set an alarm.
