# sprite_set_nineslice

This function is used to apply a [Nine Slice
struct](../Nine_Slice_Struct) to a sprite. You supply the sprite
index and the Nine Slice struct to apply, which can be retrieved using [
sprite_nineslice_create() ](sprite_nineslice_create) or [
sprite_get_nineslice() ](../Sprite_Information/sprite_get_nineslice)
. ** NOTE ** This function affects the sprite **asset** so any changes
you make with this function will affect **all** instances that are using
this sprite and all future instances too.

#### Syntax:

``` gml
sprite_set_nineslice(ind, nineslice);
```

|           |                                                                                                                          |                                   |
|-----------|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument  | Type                                                                                                                     | Description                       |
| ind       |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                         | The index of the sprite to modify |
| nineslice |  [Nine Slice Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Nine_Slice_Struct)  | The Nine Slice struct to apply    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _nineslice = sprite_nineslice_create();

_nineslice.enabled = true;
_nineslice.left = 10;
_nineslice.right = 10;
_nineslice.top = 10;
_nineslice.bottom = 10;

sprite_set_nineslice(spr_box_0, _nineslice);
```

The code above creates a new Nine Slice struct, enables it and sets the
offsets for the guides. The struct is then applied to a sprite, changing
its Nine Slice properties.
