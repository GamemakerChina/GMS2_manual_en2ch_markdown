# skeleton_slot_colour_set

With this function you can set an attachment slot colour and alpha so
all sprites attached to it will be drawn with these blend values. Keep
in mind that the instance sprite can have a blend colour and alpha
setting ( [ image_blend
](../../Sprite_Instance_Variables/image_blend) and [ image_alpha
](../../Sprite_Instance_Variables/image_angle) ), as can the
attachment (see the function [ skeleton_attachment_create_colour()
](../Attachments/skeleton_attachment_create_colour) ), and so the
final colour and alpha that the assigned attachment sprite for the slot
will have will be a composite of all these values.

#### Syntax:

``` gml
skeleton_slot_colour_set(slot, colour, alpha);
```

|          |                                                                                                                 |                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                                                            | Description                                                       |
| slot     |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The slot name to set, a string                                    |
| colour   |  [Colour](../../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to set, either an integer, a constant, or a hex value. |
| alpha    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha to set from 0 to 1.                                     |

#### Returns:

``` gml
N/A
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
