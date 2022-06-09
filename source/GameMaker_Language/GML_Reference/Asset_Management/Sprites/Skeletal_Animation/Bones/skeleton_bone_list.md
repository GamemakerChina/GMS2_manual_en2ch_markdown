# skeleton_bone_list

With this function you can populate a (pre-created) [DS
list](../../../../Data_Structures/DS_Lists/DS_Lists) with all the
names of the bones used as part of the skeletal animation sprite. The
names will be strings and can then be used in the other skeleton
animation bone functions for these types of sprite.

#### Syntax:

``` gml
skeleton_bone_list(sprite, list);
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
skeleton_bone_list(sprite_index, bone_list);
```

The above code creates a DS list then populates it with the bone names
for later use.
