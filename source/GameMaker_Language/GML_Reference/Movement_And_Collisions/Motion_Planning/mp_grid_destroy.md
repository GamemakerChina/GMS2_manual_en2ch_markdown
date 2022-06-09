# mp_grid_destroy

You can use this function to destroy the indicated mp_grid (as defined
by the function [ mp_grid_create() ](mp_grid_create) ) and free up
the memory allocated it. It is *essential* that you call this whenever
the MP grid is finished with or you could potentially get a memory leak,
meaning that your game will slow down over time and eventually crash.
**NOTE** : Using mp_grid\_\* functions on a grid after it has been
destroyed will result in an error.

#### Syntax:

``` gml
mp_grid_destroy(id);
```

|          |                                                                                                                            |                                              |
|----------|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                       | Description                                  |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be destroyed |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if timer = 0
{
    mp_grid_destroy(grid);
    room_goto(rm_Menu);
}
```

The above code will destroy the mp_grid indexed in the variable "grid"
if the variable "timer" is equal to 0, and then goto another room.
