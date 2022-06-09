# mp_grid_clear_rectangle

With this function you can define an area *in room coordinates* which
will then clear the corresponding cells in the specified MP grid. Even
if a cell partially falls within the defined rectangular region it will
be cleared.

#### Syntax:

``` gml
mp_grid_clear_rectangle(id, x1, y1, x2, y2);
```

|          |                                                                                                                            |                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                                                                       | Description                                                    |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be used                        |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The x coordinate of the left side of the rectangle to check.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The y coordinate of the top side of the rectangle to check.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The x coordinate of the right side of the rectangle to check.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The x coordinate of the bottom side of the rectangle to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
mp_grid_clear_rectangle(grid, 0, 0, 100, 200);
```

The above code will mark as free all cells of the mp_grid indexed in the
variable "grid" that fall within the area 0,0 to 100,200.
