# layer_sprite_get_index

This function can be used to get the current image index value of the
sprite element. You give the sprite element ID (which you get when you
create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and the function
will return real value that represents the image index being shown for
the sprite. The function will return -1 if either the sprite element
doesn't exist or the element doesn't have a valid sprite assigned to it.

#### Syntax:

``` gml
layer_sprite_get_index(sprite_element_id);
```

|                   |                                                                                                                                        |                                                                       |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                                           |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to get the information from |

#### Returns:

``` gml
 Real

or -1
```

#### Example:

``` gml
var lay_id = layer_get_id("sprite_sky");
var spr_id = layer_sprite_get_id(lay_id, "Clouds");
if layer_sprite_get_index(spr_id) &amp;lt; 4
{
    layer_sprite_index(spr_id, 4);
}
```

The above code will get the layer ID for the layer named "sprite_sky"
and then use that to get the ID of the sprite element on that layer.
This ID is then used to check if the image index for the element is less
than 4, and if so it is set to 4.
