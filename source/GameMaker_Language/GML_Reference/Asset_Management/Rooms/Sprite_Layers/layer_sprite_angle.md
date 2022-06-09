# layer_sprite_angle

Using this function you can change the angle for the given sprite
element on a layer. You give the sprite element ID (which you get when
you create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and then set the
angle value, from 0 to 359 anti-clockwise, where 0 is to the right, 90
is to the top, 180 is to the left and 270 is to the bottom. If you set a
value greater than 360 this will be looped to bring it within the 0 -
359 range.

#### Syntax:

``` gml
layer_sprite_angle(sprite_element_id, angle);
```

|                   |                                                                                                                                        |                                                     |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                         |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change |
| angle             |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | The angle of the sprite (default is 0)              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var asset_sprite = layer_sprite_get_id(layer, "gfc_Trees");
if layer_sprite_get_angle(asset_sprite) != 0
{
    layer_sprite_angle(asset_sprite, 0);
}
```

The above code will check the sprite element assigned to the layer the
instance running the code is on and if its angle is not 0 it will set it
to 0.
