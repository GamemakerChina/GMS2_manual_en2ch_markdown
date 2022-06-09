# layer_sprite_get_sprite

This function can be used to get the current sprite index of the sprite
element. You give the sprite element ID (which you get when you create a
sprite element using [ layer_sprite_create() ](layer_sprite_create)
or when you use the function [ layer_sprite_get_id()
](layer_sprite_get_id) ), and the function will return a real value
that represents the sprite index being shown. If the element has no
sprite assigned, the function will return -1.

#### Syntax:

``` gml
layer_sprite_get_sprite(sprite_element_id);
```

|                   |                                                                                                                                        |                                                                       |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                                           |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to get the information from |

#### Returns:

``` gml
 Sprite Element ID

or -1
```

#### Example:

``` gml
var lay_id = layer_get_id("sprite_sky");
var spr_id = layer_sprite_get_id(lay_id, "Clouds");
if layer_sprite_get_sprite(spr_id) != spr_Clouds
{
    layer_sprite_change(spr_id, spr_Clouds);
}
```

The above code will get the layer ID for the layer named "sprite_sky"
and then use that to get the ID of the sprite element on that layer.
This ID is then used to check the sprite assigned to the element,
setting it to the sprite "spr_Clouds" if it is not already.
