# mp_linear_path

This function computes a straight line path from the current instance
position to the point specified by the "xgoal" and "ygoal" values. It
uses the indicated step size, the same as in the function [
mp_linear_step() ](mp_linear_step) . The indicated path must already
exist and will be overwritten by the new path and the function will
return if a complete path was found (true) or not (false). If false is
returned then a path is still generated, but it will only run up to the
position where the path was blocked. **NOTE** : This function does not
move the instance. It sets a path only, and you must use the
[Path](../../Asset_Management/Paths/Paths) functions for movement.

#### Syntax:

``` gml
mp_linear_path(path, xgoal, ygoal, stepsize, checkall);
```

|          |                                                                            |                                                                                       |
|----------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                           |
| path     |  [Path Asset](../../../../../The_Asset_Editors/Paths)                  | The index of the path to be used.                                                     |
| xgoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The target x position.                                                                |
| ygoal    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The target y position.                                                                |
| stepsize |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The speed the instance moves in pixels per step.                                      |
| checkall |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to check for collisions with all instances (true) or just solid ones (false). |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mp_linear_path(path, obj_Player.x, obj_Player.y, 2, 0)
{
    path_start(path, 2, 0, 0);
}
```

This gets the object to check and see if there is a linear path from its
current position to the position of "obj_Player". If there is then it
starts the path.
