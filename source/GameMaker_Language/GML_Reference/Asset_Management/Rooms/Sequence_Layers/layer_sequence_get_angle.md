# layer_sequence_get_angle

With this function you supply the sequence element ID - as returned by [
layer_sequence_create() ](layer_sequence_create) or by one of the
[layer element
functions](../General_Layer_Functions/General_Layer_Functions) - and
it will return the current angle of the sequence element in the game
room. Note that angles are returned in degrees, and 0º is to the right,
90º is up, 180º is to the left and 270º is down.

#### Syntax:

``` gml
layer_sequence_get_angle(sequence_element_id)
```

|                     |                                                                                                                                              |                                                       |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument            | Type                                                                                                                                         | Description                                           |
| sequence_element_id |  [Sequence Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Sequence_Layers/layer_sequence_create)  | The unique ID value of the sequence element to target |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _ang = layer_sequence_get_angle(title_sequence)
if _ang &amp;gt; 0
{
    _ang -= 1;
    layer_sequence_angle(title_sequence, _ang);
}
```

The above code retrieves the current angle of the the sequence element
with the ID stored in the variable "title_sequence", and if it's not 0,
then 1 is subtracted form the current angle.
