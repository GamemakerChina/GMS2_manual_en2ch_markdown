# layer_sprite_change

Using this function you can change the sprite resource assigned to a
given sprite element on a layer. You give the sprite element ID (which
you get when you create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and then supply a
sprite index element asset will be changed. Note that if the sprite has
sub-images then it will animate too (this can be controlled using the [
layer_sprite_index() ](layer_sprite_index) and [
layer_sprite_speed() ](layer_sprite_speed) functions). Note that you
can assign a value of -1 as the new sprite index and no sprite will be
shown, although the element will still exist and can still be changed
again later.

#### Syntax:

``` gml
layer_sprite_change(sprite_element_id, sprite_index)
```

|                   |                                                                                                                                        |                                                     |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                         |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change |
| sprite_index      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                       | The new sprite index to use                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var s = layer_sprite_get_id(layer, global.Asset_sprite);
if layer_sprite_get_sprite(s) != spr_Nighttime
{
    layer_sprite_change(s, spr_nighttime);
}
```

The above code checks the sprite index of the element with the ID stored
in the global variable global.Asset_sprite and if it is not
"spr_Nighttime" then that sprite is assigned to the element.
