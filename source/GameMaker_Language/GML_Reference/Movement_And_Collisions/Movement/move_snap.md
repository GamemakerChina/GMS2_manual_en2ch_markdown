# move_snap

This function is used to "snap" the instance to a grid of a given size.
It will be snapped to the nearest corresponding position on the
"invisible" grid that the hsnap and vsnap values define.

#### Syntax:

``` gml
move_snap(hsnap, vsnap);
```

|          |                                                                         |                                                               |
|----------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                   |
| hsnap    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The horizontal snapping (the size in pixels between 'cells'). |
| vsnap    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The vertical snapping (the size in pixels between 'cells').   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
with (obj_Pieces)
{
    if !place_snapped(32, 32)
    {
        move_snap(32, 32);
    }
}
```

The above code checks all instances of "obj_Pieces" to see if they are
snapped to a grid of 32x32 pixels, and if they are not it snaps them to
the nearest position in that grid.
