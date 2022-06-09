# mp_linear_step

With this function you tell an instance to take a "step" towards a
specific point, specified by the xgoal and ygoal values. The size of the
step (which is how many pixels the instance should move each step) is
indicated by the stepsize, and if the instance is already at the
position it will stop and not move any further, contrary to other,
simpler functions like [ move_towards_point()
](../Movement/move_towards_point) . The stepsize is also the
distance "ahead" that the object will check each step for a collision,
and you can choose whether the instance stops at a collision with *any*
instance or only those that are flagged as solid. The function will
return whether it has reached the goal position (true) or if it has
failed (false). **NOTE** This function does not try to make detours if
it meets an obstacle, it simply fails and stops moving.

#### Syntax:

``` gml
mp_linear_step(xgoal, ygoal, stepsize, checkall);
```

|          |                                                                            |                                                                   |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                       |
| xgoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The target x position.                                            |
| ygoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The target y position.                                            |
| stepsize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The speed the instance moves in pixels per step.                  |
| checkall |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to check all instances (true) or just solid ones (false). |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mp_linear_step(mouse_x, mouse_y, 5, 0)
{
    instance_create_layer(x, y, "Effects", obj_Explosion);
    instance_destroy();
}
```

The above code will make the object move towards the mouse at a speed of
5 pixels per step. Once it reaches the mouse position it will create an
object "obj_Explosion" and destroy itself.
