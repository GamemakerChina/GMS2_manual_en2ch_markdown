# path_positionprevious

This variable can be used to get or to set the position of an instance
along its current path in the previous step, and is a normalised value
between 0 and 1 ie: 0 is the start position of the path and 1 would be
the end position. It is similar to the [ xprevious
](../../Instances/Instance_Variables/xprevious) and [ yprevious
](../../Instances/Instance_Variables/yprevious) variables in how it
works, only it is specific for paths. It can be useful for things like
temporarily stopping a path follower if something is in the way (see the
example code below).

#### Syntax:

``` gml
path_positionprevious;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _x = x + lengthdir_x(16, direction);
var _y = y + lengthdir_y(16, direction);
if collision_circle(xx, yy, 16, obj_Player, false,true)
{
    path_position = path_positionprevious;
}
```

The above code checks an area in front of the instance for a collision
with the object "obj_Player" and if there is one, it sets the instance
back to the previous position it occupied on the current path, as
assigned by the function [path_start()](../path_start) .
