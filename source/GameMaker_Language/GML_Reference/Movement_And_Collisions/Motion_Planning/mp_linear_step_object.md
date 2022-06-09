# mp_linear_step_object

With this function you tell an instance to take a "step" towards a
specific point, specified by the xgoal and ygoal values. The size of the
step (which is how many pixels the instance should move each step) is
indicated by the stepsize, and if the instance is already at the
position it will stop and not move any further, contrary to other,
simpler functions like [ move_towards_point()
](../Movement/move_towards_point) . The stepsize is also the
distance "ahead" that the object will check each step for a collision,
and you can choose whether the instance stops at a collision with an
object or instance of your choice.

#### Syntax:

``` gml
mp_linear_step_object(xgoal, ygoal, stepsize, obj);
```

|          |                                                                                                                                                                                         |                                                                                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                                  |
| xgoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target x position.                                                                                       |
| ygoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target y position.                                                                                       |
| stepsize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The speed the instance moves in pixels per step.                                                             |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object that is to block the path. Can be an object index, an instance id or the special keyword, **all** |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mp_linear_step_object(mouse_x, mouse_y, 5, obj_Wall)
{
    instance_create_layer(x, y, "Effects", obj_Explosion);
    instance_destroy();
}
```

The above code will make the object move towards the mouse at a speed of
5 pixels per step, only checking for collisions with the object
"obj_Wall". Once it reaches the mouse position it will create an object
"obj_Explosion" and destroy itself.
