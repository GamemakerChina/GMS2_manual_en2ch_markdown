# layer_sprite_x

This function controls the position along the x-axis of the room of the
asset sprite element on the layer. You give the sprite element ID (which
you get when you create a sprite element using [ layer_sprite_create()
](layer_sprite_create) or when you use the function [
layer_sprite_get_id() ](layer_sprite_get_id) ), and then set the x
value to use (based on the room coordinates).

#### Syntax:

``` gml
layer_sprite_x(sprite_element_id, x);
```

|                   |                                                                                                                                        |                                                     |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument          | Type                                                                                                                                   | Description                                         |
| sprite_element_id |  [Sprite Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sprite_Layers/layer_sprite_get_id)  | The unique ID value of the sprite element to change |
| x                 |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | The x position for the sprite                       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Asset_sky"); var spr_id = layer_sprite_get_id(lay_id, "Clouds"); layer_sprite_x(spr_id, irandom(room_width));
```

The above code gets the ID value of the sprite asset "Clouds" assigned
to the layer "Asset_sky" and then sets its x position to a random value
between 0 and the width of the room.
