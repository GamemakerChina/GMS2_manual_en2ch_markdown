# mp_potential_step_object

This function lets the instance take a step towards a particular
position defined by xgoal/ygoal, all the while trying to avoid
obstacles. When the instance would run into an instance of the object
specified by the "obj" argument it will change the direction of motion
to try to avoid that instance and move around it. This approach is not
guaranteed to work but in most easy cases it will effectively move the
instance towards the goal. The function returns whether the goal was
reached or not.

#### Syntax:

``` gml
mp_potential_step_object(xgoal, ygoal, stepsize, obj)
```

|          |                                                                                                                                                                                         |                                                                                                                                                      |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                                                                          |
| xgoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target x position.                                                                                                                               |
| ygoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target y position.                                                                                                                               |
| stepsize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The speed the instance moves in pixels per step.                                                                                                     |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object that is to block the path of the instance running the function. Can be an object index, an instance id or the special keyword , **all** . |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if instance_exists(obj_Enemy)
{
    var inst;
    inst = instance_nearest(x, y, obj_Enemy);
    mp_potential_step_object(inst.x, inst.y, 5, obj_Wall);
}
```

The above code first checks to see if there are any instances of
"obj_Enemy" in the room. If there are it then finds the nearest one and
stores its id in a variable. This variable is then used to tell
mp_potential_step_object to move the instance with the code towards the
x/y position of the object that was found at a speed of 5 pixels per
step while avoiding only instances of the object "obj_Wall".
