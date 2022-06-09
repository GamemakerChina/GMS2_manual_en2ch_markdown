# layer_sprite_index

This function can be used to set the image index of a sprite asset which
has multiple sub-images on a layer. You give the sprite element ID
(which you get when you create a sprite element using [
layer_sprite_create() ](layer_sprite_create) or when you use the
function [ layer_sprite_get_id() ](layer_sprite_get_id) ), and then
set the image index to use. If you set a value outside of the range of
sub-images, then the image index will loop around.

#### Syntax:

``` gml
layer_sprite_index(sprite_element_id, image_index);
```

|                   |                                                                                                                                        |                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                      |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to set |
| index             |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | The image index to use for the sprite            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("sprite_trees");
var spr_id = layer_sprite_get_id(lay_id, "gfc_trees");
layer_sprite_index(spr_id, 1);
```

The above code will get the layer ID for the layer named "sprite_trees"
and then use that to get the ID of the given sprite element on that
layer. This ID is then used to change the element image index.
