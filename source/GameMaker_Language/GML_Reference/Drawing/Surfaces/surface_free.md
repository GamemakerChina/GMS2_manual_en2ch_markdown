# surface_free

When you are working with surfaces, you should always use this function
whenever you are finished using them. Surfaces take up space in memory
and so need to be removed, normally at the end of a room, but it can be
done at any time depending on the use you put them to. Failure to do so
can cause memory leaks which will eventually slow down and crash your
game. **NOTE** : When working with surfaces there is the possibility
that they can cease to exist at any time due to them being stored in
texture memory. You should **ALWAYS** check that a surface exists using
[ surface_exists() ](surface_exists) before referencing them
directly.

#### Syntax:

``` gml
surface_free(surface_id);
```

|            |                                                                                                     |                                    |
|------------|-----------------------------------------------------------------------------------------------------|------------------------------------|
| Argument   | Type                                                                                                | Description                        |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to be freed. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(vk_escape)
{
    surface_free(surf);
    room_goto(rm_Menu);
}
```

The above code checks for a key press and if it detects one it frees the
memory reserved for the surface indexed in the variable "surf" and then
changes room.
