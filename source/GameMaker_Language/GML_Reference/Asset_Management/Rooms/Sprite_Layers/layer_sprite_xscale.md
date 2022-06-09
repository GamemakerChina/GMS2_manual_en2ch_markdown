# layer_sprite_xscale

Using this function you can change whether the given sprite element on a
layer should be scaled along the x axis or not. You give the sprite
element ID (which you get when you create a sprite element using [
layer_sprite_create() ](layer_sprite_create) or when you use the
function [ layer_sprite_get_id() ](layer_sprite_get_id) ), and then
set the scale value. A scale of 1 indicates no scaling (1:1), smaller
values will scale down (0.5, for example, will half the width of the
sprite used), larger values will scale up, and negative values will flip
the sprite and scale it unless the value used is exactly -1 (in which
case the sprite used is just flipped right-to-left about its origin
position with no scaling).

#### Syntax:

``` gml
layer_sprite_xscale(sprite_element_id, xscale);
```

|                   |                                                                                                                                        |                                                     |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                         |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change |
| xscale            |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | The xscale value (default is 1)                     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var asset_sprite = layer_sprite_get_id(layer, "gfc_Trees");
if layer_sprite_get_xscale(asset_sprite) != 1 || layer_sprite_get_yscale(asset_sprite) != 1
{
    layer_sprite_xscale(asset_sprite, 1);
    layer_sprite_yscale(asset_sprite, 1);
}
```

The above code will check the sprite element assigned to the layer the
instance running the code is on and if it is scaled in either direction
it will set both the x-axis scale and y-axis scale to 1.
