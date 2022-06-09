# layer_get_element_type

You can use this function to get the *element type* for the given
element. You supply the unique element ID value (for example, as
returned the function that created the element or from the room editor)
and the function will return one of the following constants (or -1 if
the element does not exist or the ID value is erroneous):

|                                                                                                                                                               |                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|  [Layer Element Type Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_element_type)  |                                                                                                                                        |
| Constant                                                                                                                                                      | Description                                                                                                                            |
|  layerelementtype_background                                                                                                                                  | The element is a background.                                                                                                           |
|  layerelementtype_instance                                                                                                                                    | The element is an instance.                                                                                                            |
|  layerelementtype_sprite                                                                                                                                      | The element is a sprite asset.                                                                                                         |
|  layerelementtype_tilemap                                                                                                                                     | The element is a tilemap.                                                                                                              |
|  layerelementtype_particlesystem                                                                                                                              | The element is a particle system.                                                                                                      |
|  layerelementtype_tile                                                                                                                                        | The element is a legacy background tile (this is only valid for projects that have been imported from previous versions of GameMaker). |
|  layerelementtype_sequence                                                                                                                                    | The element is a sequence asset.                                                                                                       |

Note that this function is most useful when you have multiple different
element types assigned to the one layer, and that you can get a list of
all the elements on any given layer using the function [
layer_get_all_elements() ](layer_get_all_elements) .

#### Syntax:

``` gml
layer_get_element_type(element_id)
```

|          |                                                                                                                                                    |                                                       |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                                                                               | Description                                           |
| layer    |  [Layer Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_all_elements)  | The unique ID value of the element to get the type of |

#### Returns:

``` gml
 Layer Element Type Constant

or -1 (if element does not exist or is invalid)
```

#### Example:

``` gml
var a = layer_get_all_elements(layer);
for (var i = 0; i &amp;lt; array_length(a); i++;)
{
    if layer_get_element_type(a[i]) == layerelementtype_sprite
    {
        layer_sprite_destroy(a[i])
    }
}
```

The above code gets the IDs for all the instance elements assigned to
the layer of the instance running the code. The code then checks to see
if any of the returned elements are sprite assets and if they then they
are destroyed.
