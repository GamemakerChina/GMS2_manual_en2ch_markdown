# layer_sequence_is_paused

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will check if the sequence is currently paused or not, returning true
if it is paused, and false if it is not.

#### Syntax:

``` gml
layer_sequence_is_paused(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if layer_sequence_is_paused(title_sequence) != 0
{
    layer_sequence_play(title_sequence);
}
```

The above code checks if the sequence element ID stored in the variable
"title_sequence" is paused, and if it is it starts it playing.
