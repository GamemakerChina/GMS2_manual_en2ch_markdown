# physics_apply_angular_impulse

This function will give an angular impulse to a physics enabled
instance. This impulse will set the angular rotation by the amount
given, ignoring the current torque, essentially setting the amount of
"spin" that a fixture has. If you wish to apply an angular force to an
instance using torque, then you should be using the function [
physics_apply_torque() ](physics_apply_torque) .

#### Syntax:

``` gml
physics_apply_angular_impulse(impulse)
```

|          |                                                                         |                                              |
|----------|-------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                    | Description                                  |
| impulse  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The impulse (in Newton metres) to be applied |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check(vk_up)
{
    physics_apply_angular_impulse(10);
}
```

The code above will give the physics enabled fixture an angular impulse
if a key is pressed.
