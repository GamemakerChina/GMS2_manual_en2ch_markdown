# sprite_nineslice_create

* Nine Slicing is a technique used to scale rectangular images for
preserving details, making them retain their original form after
scaling. See [this
page](../../../../../The_Asset_Editors/Sprite_Properties/Nine_Slices)
for information on Nine Slice.* This function is used to create a Nine
Slice [struct](../../../../GML_Overview/Structs) which can be
modified and then applied to a sprite. The contents of this struct are
detailed on [this page](../Nine_Slice_Struct) . You can store this
struct in a variable, modify its properties, and apply it to any sprites
using [sprite_set_nineslice()](sprite_set_nineslice) .

#### Syntax:

``` gml
sprite_nineslice_create();
```

#### Returns:

``` gml
 Nine Slice Struct
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
