# sequence_exists

With this function you can check to see if a sequence object exists or
not. You supply either the sequence object struct (as returned by the
function [ sequence_create() ](sequence_create) or [ sequence_get()
](sequence_get) ) or the sequence ID (as returned by the function [
layer_sequence_get_sequence()
](../Rooms/Sequence_Layers/layer_sequence_get_sequence) or from the
sequence instance struct property sequence , or the index from the asset
browser) and the function will return true if the sequence object exists
or false if it does not.

#### Syntax:

``` gml
sequence_exists(sequence_struct_or_id);
```

|                       |                                                                                                                                                                                                                              |                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Argument              | Type                                                                                                                                                                                                                         | Description                                                                                 |
| sequence_struct_or_id |  [Sequence Asset](../../../../../The_Asset_Editors/Sequences) or [Sequence Object Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Sequence_Object_Struct)    | The sequence to check for, can be the asset reference itself or its Sequence object struct. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if sequence_exists(my_seq)
{
    sequence_destroy(my_seq);
}
```

The above code checks to see if the given sequence object exists and if
it does it is destroyed.
