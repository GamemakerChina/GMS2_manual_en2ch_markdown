# object_set_mask

With this function you can set the mask_index of a specific object (for
more information on masks see [The Object
Editor](../../../../The_Asset_Editors/Objects) ). This means that
all instances of this object that are created *after the mask has been
changed* will be created with this new mask, while instances that are
already in the room may not be affected. You can set this to -1 to
remove a mask sprite and so default to the mask defined for the sprite
of the object (or no masks if no sprite has been chosen). Please note
that this is not an instance function! You can set the mask index of
individual instances using the [ mask_index
](../Sprites/Sprite_Instance_Variables/mask_index) variable and so
have ten instances all with a different mask to the object they are
created from, and even if you change the mask index of the object using
this function, all instances that are currently in the room will remain
as they were, and only instances created after calling the function will
start with the new mask.

#### Syntax:

``` gml
object_set_mask(index, spr);
```

|          |                                                                |                                             |
|----------|----------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                           | Description                                 |
| index    |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The index of the object to change.          |
| spr      |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)  | The new sprite to use as the object's mask. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.level == 10)
{
    object_set_mask(obj_Platform, spr_mask_10);
}
```

The above code checks the value of global variable and then changes the
mask index of the object "obj_Platform" if it is equal to ten.
