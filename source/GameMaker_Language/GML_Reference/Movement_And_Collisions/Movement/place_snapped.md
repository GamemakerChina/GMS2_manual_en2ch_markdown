# place_snapped

With this function you can check and see if the origin of an instance
(its x and y position) is aligned to a grid with the hsnap and vsnap
values specified by you.

#### Syntax:

``` gml
place_snapped(hsnap, vsnap);
```

|          |                                                                         |                                   |
|----------|-------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                    | Description                       |
| hsnap    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The horizontal snapping to check. |
| vsnap    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The vertical snapping to check.   |

#### Returns:

``` gml
 Boolean
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
