# The Nine Slice Struct

A Nine Slice [struct](../../../GML_Overview/Structs) can be created
using [ sprite_nineslice_create()
](Sprite_Manipulation/sprite_nineslice_create) , or retrieved from a
sprite using [ sprite_get_nineslice()
](Sprite_Information/sprite_get_nineslice) . This struct will
contain properties that can be changed and applied to a sprite using [
sprite_set_nineslice() ](Sprite_Manipulation/sprite_set_nineslice) .
If retrieved from a sprite, changing values in this struct **will**
affect the original sprite. The following properties will be available
in this struct:

|                                                                                                                       |                                                                                                                                                                                                  |                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Nine Slice Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Nine_Slice_Struct)  |                                                                                                                                                                                                  |                                                                                                                                                                                     |
| Variable                                                                                                              | Type                                                                                                                                                                                             | Description                                                                                                                                                                         |
|  enabled                                                                                                              |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                        | This boolean will be **true** if Nine Slicing is enabled for the sprite, and **false** if it is disabled. You can modify this to enable or disable Nine Slicing for the sprite.     |
|  left                                                                                                                 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                           | This is the offset for the left guide on the x axis, relative to the left edge of the sprite.                                                                                       |
|  right                                                                                                                |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                           | This is the offset for the right guide on the x axis, relative to the right edge of the sprite.                                                                                     |
|  top                                                                                                                  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                           | This is the offset for the top guide on the y axis, relative to the top edge of the sprite.                                                                                         |
|  bottom                                                                                                               |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                           | This is the offset for the bottom guide on the y axis, relative to the bottom edge of the sprite.                                                                                   |
|  tilemode                                                                                                             |  [Array](../../../../../GameMaker_Language/GML_Overview/Arrays) of [Tile Mode Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Nine_Slice_Struct) s    | This returns an [array](../../../GML_Overview/Arrays) containing the **Tile Modes** for the edge and centre slices.                                                             |

## Tile Modes

The **Tile Mode** of each slice can be read or modified using these
constants as the array index:

|                                                                                                                              |                       |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------|
|  [Nine Slice Edge Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Nine_Slice_Struct)  |                       |
| Constant                                                                                                                     | Description           |
|  nineslice_left                                                                                                              | The left edge slice   |
|  nineslice_top                                                                                                               | The top edge slice    |
|  nineslice_right                                                                                                             | The right edge slice  |
|  nineslice_bottom                                                                                                            | The bottom edge slice |
|  nineslice_centre                                                                                                            | The centre slice      |

The **Tile Mode** for a slice will be (or can be set to) one of the
following constants:

|                                                                                                                        |                                                                                 |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
|  [Tile Mode Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Nine_Slice_Struct)  |                                                                                 |
| Constant                                                                                                               | Description                                                                     |
|  nineslice_stretch                                                                                                     | The slice will be stretched                                                     |
|  nineslice_repeat                                                                                                      | The slice will be repeated                                                      |
|  nineslice_mirror                                                                                                      | The slice will be repeated by mirroring                                         |
|  nineslice_blank                                                                                                       | The slice will not be stretched or repeated, resulting in a blank area after it |
|  nineslice_hide                                                                                                        | The slice will not appear at all                                                |

Since **tilemode** is an array, you need to use the array syntax to
change the Tile Mode of a slice. The code example below sets the Tile
Mode of the top slice to **Repeat** :

#### Example:

``` gml
var _nineslice = sprite_get_nineslice(spr_box);

_nineslice.tilemode[nineslice_top] = nineslice_repeat;
```

See [this
page](../../../../The_Asset_Editors/Sprite_Properties/Nine_Slices)
for more information on the Nine Slice technique.
