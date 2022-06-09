# layer_background_sprite

Using this function you can set the sprite index of the background
element. You supply the background element ID (which you get when you
create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and then
give a sprite index to be used. The background element image will be
replaced with the new sprite. If you give a value of -1, the element
will have no sprite assigned (but will still exist and can have a sprite
assigned again later). This function also has the alias
layer_background_change() .

#### Syntax:

``` gml
layer_background_sprite(background_element_id, sprite_index)
```

|                       |                                                                                                                                                    |                                                                  |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                      |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change          |
| sprite_index          |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                                   | The sprite index of the sprite to use for the background element |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky");
var back_id = layer_background_get_id(lay_id);
if layer_background_get_sprite(back_id) != spr_Clouds
{
    layer_background_sprite(back_id, spr_Clouds);
}
```

The above code will get the layer ID for the layer named
"Background_sky" and then use that to get the ID of the background
element on that layer. This ID is then used to check the sprite assigned
to the element, setting it to the sprite "spr_Clouds" if it is not
already.
