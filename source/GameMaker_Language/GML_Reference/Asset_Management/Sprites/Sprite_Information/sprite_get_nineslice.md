# sprite_get_nineslice

This function returns the [Nine Slice struct](../Nine_Slice_Struct)
for a sprite, containing all its Nine Slice properties as set in the
[Sprite Editor](../../../../../The_Asset_Editors/Sprites) or using
[sprite_set_nineslice()](../Sprite_Manipulation/sprite_set_nineslice)
. The contents of this struct are detailed on [this
page](../Nine_Slice_Struct) . If the supplied sprite does not have a
Nine Slice struct assigned to it, a new struct with default Nine Slice
properties will be created for the sprite and returned. Changing any
values in this struct **will** modify the Nine Slice properties of the
original sprite, affecting any future draw calls made with that sprite.

#### Syntax:

``` gml
sprite_get_nineslice(ind);
```

|          |                                                                   |                                                                            |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                              | Description                                                                |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite from which the Nine Slice struct will be retrieved |

#### Returns:

``` gml
 Nine Slice Struct

(or -1 if the sprite doesn't exist)
```

#### Example:

``` gml
var _box_nineslice = sprite_get_nineslice(spr_box_0);

_box_nineslice.enabled = true;
_box_nineslice.left = 10;
_box_nineslice.right = 10;
_box_nineslice.top = 10;
_box_nineslice.bottom = 10;
```

The code above retrieves the Nine Slice struct from a sprite, enables
Nine Slicing for it and sets the guide offsets.
