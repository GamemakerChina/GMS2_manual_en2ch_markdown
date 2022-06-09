# mp_linear_path_object

This function computes a straight line path from the current instance
position to the point specified by the "xgoal" and "ygoal" values. It
uses the indicated step size, the same as in the function [
mp_linear_step() ](mp_linear_step) . The indicated path must already
exist and will be overwritten by the new path and the function will
return if a complete path was found (true) or not (false). A full path
is only found there was no collision with the specified object or
instance and if false is returned then a path is still generated, but it
will only run up to the position where the path was blocked. **NOTE** :
This function does not move the instance. It sets a path only, and you
must use the [Path](../../Asset_Management/Paths/Paths) functions
for movement.

#### Syntax:

``` gml
mp_linear_path_object(path, xgoal, ygoal, stepsize, obj);
```

|          |                                                                                                                                                                                         |                                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                                   |
| path     |  [Path Asset](../../../../../The_Asset_Editors/Paths)                                                                                                                               | The index of the path to be used                                                                              |
| xgoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target x position.                                                                                        |
| ygoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The target y position.                                                                                        |
| stepsize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The speed the instance moves in pixels per step.                                                              |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object that is to block the path. Can be an object index, an instance id or the special keyword , **all** |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mp_linear_path_object(path, mouse_x, mouse_y, 4, obj_Wall)
{
    path_start(path, 4, 0, 0);
}
```

The above code checks for a collision with "obj_Wall" along the path
between the object running the code and the x/y position of the mouse.
If there is no collision and the complete path is generated then it will
start the object along the path generated.
