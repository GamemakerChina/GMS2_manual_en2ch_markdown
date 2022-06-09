# layer_sequence_destroy

With this function you can destroy (remove from the room) a sequence
element. You supply the sequence element ID as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) and
the sequence will be destroyed.

#### Syntax:

``` gml
layer_sequence_destroy(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var a = layer_get_all_elements(layer);
for (var i = 0; i &amp;lt; array_length(a); i++;)
{
    if layer_get_element_type(a[i]) == layerelementtype_sequence
    {
        layer_sequence_destroy(a[i])
    }
}
```

The above code gets the IDs for all the elements assigned to the layer
of the instance running the code. The code then checks to see if any of
the returned elements are sequence assets and if they then they are
destroyed.
