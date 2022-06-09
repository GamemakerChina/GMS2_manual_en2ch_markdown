# move_outside_all

With this function you can tell an instance to move out of a collision
in any direction and any number of pixels each step, with a value of -1
or 0 for the maxdist being a default 1000px, ie: GameMaker will move the
instance continually up 1000 pixels until it is out of collision.

#### Syntax:

``` gml
move_outside_all(dir, maxdist);
```

|          |                                                                         |                                                                                      |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                          |
| dir      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The direction to move in.                                                            |
| maxdist  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum distance the object can travel (-1 or 0 a default value of 1000 pixels). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if place_meeting(x, y, all)
{
    move_outside_all(90, 1);
}
```

The above code will move the instance up 1 pixel each step that it is in
collision with any other instance.
