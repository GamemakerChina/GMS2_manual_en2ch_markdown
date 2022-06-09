# skeleton_attachment_get

A skeletal animation sprite may have other sprites added as attachments,
with these sprites being added to a named slot (the name is given when
you create the attachment slot in your animation program) and they will
be drawn along with the animation of the current sprite. With this
function you can get the name (as a string) of the attachment for the
given slot of the currently assigned sprite. Note that attached sprites
are referenced through their *name string* as assigned in Spine, or when
you called [ skeleton_attachment_create()
](skeleton_attachment_create) .

#### Syntax:

``` gml
skeleton_attachment_get(slot);
```

|          |                                                                                 |                                                    |
|----------|---------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                            | Description                                        |
| slot     |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The slot name (a string) to get the attachment of. |

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
