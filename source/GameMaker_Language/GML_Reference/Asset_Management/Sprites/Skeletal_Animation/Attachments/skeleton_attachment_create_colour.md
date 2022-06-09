# skeleton_attachment_create_colour

When you create you skeletal animation sprite, you can assign
*attachment slots* and *attachments* to go in them. These are simply
images (sprites) that are separate from the animation but when attached
will move along with the bone they are attached to. Normally you would
assign these attachments in your animation program (Spine), but with
this function you can create your own at run-time using a sprite asset
from your game. the function requires that you give the attachment a
name (as a string) and then set the [ sprite_index
](../../Sprite_Instance_Variables/sprite_index) and [ image_index
](../../Sprite_Instance_Variables/image_index) to use, as well as
the x and y origin (which can be different to that defined by the sprite
in the sprite properties), and you can also set any transforms that you
wish to be applied to the image when attached, as well as the colour to
be blended with the image and it's alpha (transparency) value. If the
attachment was successfully created the function will return 1 and if it
was not (you supplied an invalid sprite index, or the base sprite is not
a Spine sprite) then it will return -1 . It is worth noting that the
instance sprite can have a blend colour and alpha setting ( [
image_blend ](../../Sprite_Instance_Variables/image_blend) and [
image_alpha ](../../Sprite_Instance_Variables/image_alpha) ), as can
the attachment slot (see the function [ skeleton_slot_colour_set()
](../Slots/skeleton_slot_colour_set) ), and so the final colour and
alpha that the assigned attachment sprite for the slot will have will be
a composite of all these values.

#### Syntax:

``` gml
skeleton_attachment_create_colour(name, sprite, ind, xorigin, yorigin, xscale, yscale, rot, colour, alpha);
```

|          |                                                                                                                 |                                                                                              |
|----------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                            | Description                                                                                  |
| name     |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                  | The name (as a string) of the attachment to create.                                          |
| sprite   |  [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)                                             | The sprite_index to get the attachment image from.                                           |
| ind      |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The image_index to get the attachment image from.                                            |
| xorigin  |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x origin for the image being used.                                                       |
| yorigin  |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y origin for the image being used.                                                       |
| xscale   |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The horizontal scaling of the image, as a multiplier: 1 = normal scaling, 0.5 is half etc... |
| yscale   |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The vertical scaling of the image, as a multiplier: 1 = normal scaling, 0.5 is half etc...   |
| rot      |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The rotation of the image: 0 = normal, 90 = turned 90° counter-clockwise etc.                |
| Colour   |  [Colour](../../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour value to use (A constant, integer or hex value).                                  |
| Alpha    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The alpha value to use (from 0 to 1).                                                        |

#### Returns:

``` gml
 Real

(1 if successful, -1 if not)
```

#### Example:

``` gml
skeleton_attachment_create_colour("sword", spr_Weapons, 0, 0, 80, 1, 1, 90, c_red, 1);
skeleton_attachment_create_colour("knife", spr_Weapons, 1, 0, 45, 1, 1, 90, c_yellow, 1);
skeleton_attachment_create_colour("crossbow", spr_Weapons, 0, 10, 30, 1, 1, 0, c_white, 0.5);
skeleton_attachment_set("slot_leftHand", choose("sword", "knife", "crossbow"));
```

The above code would check the currently assigned attachment name for
the slot named "slot_leftHand" and if an empty string is returned, a new
sprite is attached.
