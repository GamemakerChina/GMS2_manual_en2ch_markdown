# position_empty

This function will check to see if a given position enters into
collision with *any instance* with a valid collision mask at the given
position.

#### Syntax:

``` gml
position_empty(x, y);
```

|          |                                                                         |                          |
|----------|-------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                    | Description              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position to check. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var xx, yy;
xx = random(room_width);
yy = random(room_height);
if position_empty(xx, yy)
{
    instance_create_layer(xx, yy, "Bullets", obj_Bomb);
}
```

This will check a random position somewhere in the room for a collision
and if there is none it will create an instance of obj_Bomb.
