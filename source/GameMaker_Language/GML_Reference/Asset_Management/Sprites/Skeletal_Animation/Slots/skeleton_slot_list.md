# skeleton_slot_list

With this function you can populate a (pre-created) DS list with all the
names of the slots created as part of the skeletal animation sprite. The
names will be strings and can then be used in the other skeleton
animation slot functions for these types of sprite.

#### Syntax:

``` gml
skeleton_slot_list(sprite, list);
```

|          |                                                                                                                   |                                                                        |
|----------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Argument | Type                                                                                                              | Description                                                            |
| sprite   |  [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)                                               | The sprite index of the Spine skeletal animation to get the list from. |
| list     |  [DS List ID](../../../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The ID of the DS list to populate with the bone names.                 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
bone_list = ds_list_create();
skeleton_slot_list(sprite_index, bone_list);
```

The above code creates a DS list then populates it with the slot names
for later use.
