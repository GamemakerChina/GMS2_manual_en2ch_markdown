# layer_background_destroy

This function will destroy the given background element. You supply the
background ID (which you get when you create the background using [
layer_background_create() ](layer_background_create) or when you use
the layer ID along with [ layer_get_background_id()
](layer_background_get_id) ) and this will remove it. Note that this
does *not* remove the layer, only the background from it, and if the
background is one that has been added in the room editor, then the next
time you leave the room and then return, the background will be
recreated again. However if the room is persistent, the background will
be removed unless room persistence is switched off again.

#### Syntax:

``` gml
layer_background_destroy(background_element_id)
```

|                       |                                                                                                                                                    |                                                               |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                   |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to be destroyed |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_trees");
var bck_id = layer_background_get_id("Forrest");
if layer_background_exists(lay_id, bck_id)
{
    layer_background_destroy(bck_id);
}
```

The above code checks the layer "Background_trees" to see if the given
background element exists and if it does, then it is destroyed (but not
the layer).
