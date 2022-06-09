# move_bounce_all

With this function you can command an instance to bounce off **all**
instances within the room, with the only exception being those that have
no sprite or mask index assigned to them. You can also tell it to use
precise collision checking when enabled, but be aware that this requires
all instances to have precise masks enabled and will greatly slow down
your game when many instances are involved due to the amount of
processing that has to be done. This should normally go in the step
event of an instance, but can be used selectively in a collision event
too, as illustrated by the code example below.

#### Syntax:

``` gml
move_bounce_all( adv );
```

|          |                                                                            |                                                            |
|----------|----------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                |
| adv      |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to enable advanced bouncing (true) or not (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if other.visible
{
    move_bounce_all(false);
}
```

The above code would be placed in a collision event with another object.
It first checks to see if the object is visible and if it is it then
performs the move_bounce_all() action. Note that in this case the bounce
is selective and will only be calculated for this collision, rather than
for every instance, every step.
