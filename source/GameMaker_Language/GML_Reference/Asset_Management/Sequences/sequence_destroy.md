# sequence_destroy

With this function you can destroy a sequence object that has been
created dynamically. You supply either the sequence object struct (as
returned by the function [ sequence_create() ](sequence_create) ) or
the sequence ID (as returned by the function [
layer_sequence_get_sequence()
](../Rooms/Sequence_Layers/layer_sequence_get_sequence) or from the
sequence instance struct property sequence ). This function should be
used whenever a dynamically created sequence is no longer required to
free up the memory associated with it.

#### Syntax:

``` gml
sequence_destroy(sequence_struct_or_id);
```

|                       |                                                                                                                                                                                                                              |                                             |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument              | Type                                                                                                                                                                                                                         | Description                                 |
| sequence_struct_or_id |  [Sequence Asset](../../../../../The_Asset_Editors/Sequences) or [Sequence Object Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Sequence_Object_Struct)    | The sequence object struct or ID to destroy |

#### Returns:

``` gml
N/A
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
