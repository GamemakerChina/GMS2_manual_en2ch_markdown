# skeleton_skin_list

With this function you can populate a (pre-created) [DS
list](../../../../Data_Structures/DS_Lists/DS_Lists) with all the
names of the skins included as part of the skeletal animation sprite.
The names will be strings and can then be used in the other skeleton
animation skin functions for these types of sprite.

#### Syntax:

``` gml
skeleton_skin_list(sprite, list);
```

|          |                                                                                                                   |                                                                        |
|----------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Argument | Type                                                                                                              | Description                                                            |
| sprite   |  [Sprite Asset](../../../../../../../The_Asset_Editors/Sprites)                                               | The sprite index of the Spine skeletal animation to get the list from. |
| list     |  [DS List ID](../../../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The ID of the DS list to populate with the animation names.            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var list = ds_list_create();
skeleton_skin_list(sprite_index, list);
var num = ds_list_size(list);
skeleton_skin_set(list[| irandom(num - 1));
ds_list_destroy(list);
```

The above code creates a DS list then populates it with the skin names.
A random one is then chosen and applied to the instance before the list
is destroyed.
