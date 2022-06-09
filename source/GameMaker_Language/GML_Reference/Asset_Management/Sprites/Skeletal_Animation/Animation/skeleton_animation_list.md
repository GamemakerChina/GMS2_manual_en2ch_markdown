# skeleton_animation_list

With this function you can populate a (pre-created) [DS
list](../../../../Data_Structures/DS_Lists/DS_Lists) with all the
names of the animations included as part of the skeletal animation
sprite. The names will be strings and can then be used in the other
animation functions for these types of sprite.

#### Syntax:

``` gml
skeleton_animation_list(sprite, list);
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
skeleton_animation_list(sprite_index, list);

for (var i = 1; i &amp;lt; ds_list_size(list); i++;)
{
    skeleton_animation_mix(list[| 0], list[| i], 0.5);
}

ds_list_destroy(list);
```

The above code creates a DS list of all the animation names for the
sprite being used by the instance. It then loops through these and sets
the mix value for all of them with the first animation to 0.5.
