# mp_grid_draw

This function will draw the specified MP grid (as defined by [
mp_grid_create() ](mp_grid_create) ), marking free cells as green
and forbidden cells as red. This function is essential as a debug tool
but it should be noted that it is *very* slow and only works when used
in the **draw** event of the instance, and that you can set the draw
alpha to change the opacity of the grid, permitting you to draw it as an
overlay and see what is actually in the room at the same time.

#### Syntax:

``` gml
mp_grid_draw(id);
```

|          |                                                                                                                            |                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                                       | Description                              |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be drawn |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
draw_set_alpha(0.3);
mp_grid_draw(grid);
draw_set_alpha(1);
```

The above code will draw the mp_grid indexed in the variable "grid" as a
semi-transparent overlay (but only if the instance running the code has
a depth lower than all the rest).
