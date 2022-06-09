# mp_grid_clear_all

With this function you can clear an MP grid of all "forbidden" cells.

#### Syntax:

``` gml
mp_grid_clear_all(id);
```

|          |                                                                                                                            |                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                       | Description                             |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be used |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !instance_exists(obj_Player)
{
    mp_grid_clear_all(grid);
}
```

The above code will clear the mp_grid indexed in the variable "grid",
marking all the cells as free, if an instance of the object "obj_Player"
no longer exists in the room.
