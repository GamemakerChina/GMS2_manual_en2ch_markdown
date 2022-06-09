# layer_sequence_exists

With this function you can check to see if a sequence element exists on
the given layer. You supply the layer ID which can be a string of the
layer name - as defined in the room editor - or the unique layer ID - as
returned by the function [ layer_get_id()
](../General_Layer_Functions/layer_get_id) , as well the sequence
element ID - as returned by [ layer_sequence_create()
](layer_sequence_create) or by one of the [layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return true if the given element exists or false otherwise.

#### Syntax:

``` gml
layer_sequence_exists(layer_id, sequence_element_id)
```

|                     |                                                                                                                                                                                                                  |                                                       |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                                                                                             | Description                                           |
| layer_ID            |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID or name of the layer to check           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)                                                                      | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !layer_sequence_exists("Background", my_seq)
{
    my_seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
    layer_sequence_pause(my_seq);
}
```

The above code checks to see if the given sequence element exists, and
if it does not then it creates a new sequence on the given layer then
pauses it.
