# ds_grid_create

With this function you can create a new DS grid data structure of the
specified cell width and height. This function returns an id which must
be used in all further functions that deal with this DS grid.
**IMPORTANT!** When you create a data structure, the index value to
identify it is an integer value starting at 0. This means that data
structures of different types can have the **same** index value, so if
in doubt you should be using the [ ds_exists() ](../ds_exists)
function before accessing them. Also note that indices are re-used, so a
destroyed data structure index value may be used by a newly created one
afterwards.

#### Syntax:

``` gml
ds_grid_create(w, h);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the grid to be created.  |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the grid to be created. |

#### Returns:

``` gml
 DS Grid ID
```

#### Example:

``` gml
mygrid = ds_grid_create(10, 10)
```

This creates a grid 10 cells high and 10 cells wide.
