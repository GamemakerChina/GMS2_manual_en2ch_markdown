# layer_background_create

With this function you can assign a sprite resource to a layer to be
used as a background in your project. You supply the layer ID (which you
get when you create the layer using [ layer_create()
](../General_Layer_Functions/layer_create) ) or the layer name (as a
string - this will have a performance impact) and a sprite index (which
would be the name of the sprite as shown in the Asset Browser), and it
will be added to the layer. The function returns the unique ID value for
the element, which can then be used in further layer functions for
backgrounds.

#### Syntax:

``` gml
layer_background_create(layer_id, sprite)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| sprite   |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)                                                                                                                                                 | The sprite index to be used                                                |

#### Returns:

``` gml
 Background Element ID
```

#### Example:

``` gml
global.back_layer = layer_create(10000);
global.back_trees = layer_background_create(global.back_layer, spr_Trees);
```

The above code creates a new layer and then adds a new background
element to it, setting a sprite to be the background image used.
