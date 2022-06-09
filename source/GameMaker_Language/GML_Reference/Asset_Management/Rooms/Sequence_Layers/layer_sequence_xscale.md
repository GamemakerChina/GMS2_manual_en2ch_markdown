# layer_sequence_xscale

With this function you can set the X scale for the given sequence
element. You supply the sequence element ID as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) along
with the new scale to set on the X axis and the sequence will be scaled
by this amount. A scale of 1 indicates no scaling (1:1), smaller values
will scale down (0.5, for example, will half the width of the sequence),
larger values will scale up and negative values will mirror the sequence
about its origin *and* scale it unless the value used is exactly -1 (in
which case the sequence is just mirrored about its origin with no
scaling). It is very important to note that applying *uneven* scaling
(eg: scaling the X axis by 3 and the Y axis by 2) to sequence elements
that contain any instance which uses *rotation* , **may cause issues
with the instance drawing, collisions, culling, and many other things**
. Basically, if your sequence relies on *any* instance properties then
we do not recommend that you combine uneven scaling along with instance
rotation. Also note that you shouldn't change the image_xscale \\
image_yscale \\ image_angle \\ x \\ y variables for any instances in a
sequence that uses this function as they will be overwritten as soon as
the sequence updates after calling the function.

#### Syntax:

``` gml
layer_sequence_xscale(sequence_element_id, xscale)
```

|                     |                                                                                                                                              |                                                             |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                                 |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target       |
| xscale              |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                    | The new X axis scale value to apply to the sequence element |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if seq_scale &amp;lt; 2
{
    seq_scale += 0.01;
    layer_sequence_xscale(my_seq, seq_scale);
    layer_sequence_yscale(my_seq, seq_scale);
}
```

The above code checks the value held in the seq_scale variable, and if
it is less than 2 then it adds to it then uses the value to set the X
and Y scale of the sequence element referenced in the variable my_seq .
