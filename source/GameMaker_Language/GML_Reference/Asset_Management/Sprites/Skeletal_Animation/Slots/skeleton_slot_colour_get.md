# skeleton_slot_colour_get

With this function you can get an attachment slot colour. You supply the
slot name (a string) and the function will return an integer value for
the colour.

#### Syntax:

``` gml
skeleton_slot_colour_get(slot);
```

|          |                                                                                 |                                  |
|----------|---------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                            | Description                      |
| slot     |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The slot name to check, a string |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
slot_list = ds_list_create();
skeleton_find_slot(mouse_x, mouse_y, slot_list);
if !ds_list_empty(slot_list)
{
    for (var i = 0; i &amp;lt; ds_list_size(slot_list); ++i)
    {
        if skeleton_slot_colour_get(slot_list[| i]) != c_white
        {
            skeleton_slot_colour_set(slot_list[| i], c_white, 1);
        }
    }
}
```

The above code creates a DS list and then populates it with the slot
names found at the position of the mouse in the room. It then loops
through the slot list and resets the colour for the found slots to white
with an alpha of 1 if the colour is not already white.
