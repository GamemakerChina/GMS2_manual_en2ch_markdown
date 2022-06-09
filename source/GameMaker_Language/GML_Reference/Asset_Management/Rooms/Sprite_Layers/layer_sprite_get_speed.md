# layer_sprite_get_speed

This function can be used to get the current speed multiplier value of
the sprite element. You give the sprite element ID (which you get when
you create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and the function
will return real value that represents the speed multiplier being used
to animate the sprite. Default value is 1.

#### Syntax:

``` gml
layer_sprite_get_speed(sprite_element_id);
```

|                   |                                                                                                                                        |                                                                       |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                                           |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to get the information from |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var lay_id = layer_get_id("sprite_sky");
var spr_id = layer_sprite_get_id(lay_id, "Clouds");
if layer_sprite_get_speed(spr_id) &amp;gt; 0
{
    layer_sprite_speed(spr_id, 0);
}
```

The above code will get the layer ID for the layer named "sprite_sky"
and then use that to get the ID of the sprite element on that layer.
This ID is then used to check the animation speed for the element and if
it is greater than 0, it is set to 0.
