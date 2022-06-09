# skeleton_attachment_set

A skeletal animation sprite may have other images added as attachments,
with these images being added to a named slot (the name is given when
you create the attachment slot in your animation program) and they will
be drawn along with the animation of the current sprite. With this
function you can set an attachment to a given slot, where you are
required to give the names (as strings) of the slot and the attachment.
These names are defined by the animation program used, or (in the case
of the attachment) when you call [ skeleton_attachment_create()
](skeleton_attachment_create) . Note that you can also pass a
sprite_index in as the attachment, and that sprite will be used, or you
can use -1 to remove the attachment from the slot. When you pass a
sprite index in as an argument, it will create an attachment slot using
the name of the sprite as the string to name the slot (so using
spr_sword , for example, will create an attachment slot "spr_sword"),
and the slot will use the first image index (0) of the the sprite, as
well as its x and y origin offset, with a scale of (1,1) and a rotation
of 0.

#### Syntax:

``` gml
skeleton_attachment_set(slot, attachment);
```

|            |                                                                                                                                                         |                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument   | Type                                                                                                                                                    | Description                                                       |
| slot       |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The slot name (a string) to get the attachment of.                |
| attachment |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)    | The name (as a string or a sprite_index) of the attachment image. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if skeleton_attachment_get("slot_leftHand") == ""
{
    skeleton_attachment_set("slot_leftHand", choose("sword", "spear", "knife"));
}
```

The above code would check the currently assigned attachment name for
the slot named "slot_leftHand" and if an empty string is returned, a new
sprite is attached.
