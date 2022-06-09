# physics_world_update_speed

GameMaker updates things based on the room speed, so that if you set it
to ,say, 30, GameMaker will run 30 steps in the course of a second.
However, for the physics functions that may not be enough and you may
want things to be updated at a slightly faster speed to increase
stability or precision. To that end we use the function
physics_world_update_speed() which sets the update speed for the physics
system *independently* of the room speed. This means that you could have
a room speed of 30, but set the physics to 60, effectively doubling the
speed at which the physics system updates and performs its calculations
compared to the speed at which the step are updated. **NOTE** : you
cannot currently set this to any less than room speed, but future
updates may change this.

#### Syntax:

``` gml
physics_world_update_speed(speed)
```

|          |                                                                         |                                                                |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                    |
| speed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of times per second that the physics system updates |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_world_update_speed(room_speed * 2);
```

The code above sets the physics system update speed to be twice that of
the room speed.
