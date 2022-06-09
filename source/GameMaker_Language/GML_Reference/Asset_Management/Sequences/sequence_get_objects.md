# sequence_get_objects

With this function you can retrieve an
[array](../../../GML_Overview/Arrays) of all the object indices that
have instances being created within the given sequence. You supply
either the sequence object struct (as returned by the function [
sequence_create() ](sequence_create) or [ sequence_get()
](sequence_get) ) or the sequence ID (as returned by the function [
layer_sequence_get_sequence()
](../Rooms/Sequence_Layers/layer_sequence_get_sequence) or from the
sequence instance struct property sequence ) and the function will
return an array, where each item in the array is an [ object_index
](../Objects/object_index) for the different objects being used by
the sequence to create instances.

#### Syntax:

``` gml
sequence_get_objects(sequence_struct_or_id);
```

|                       |                                                                                                                                                                                                                              |                                                           |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument              | Type                                                                                                                                                                                                                         | Description                                               |
| sequence_struct_or_id |  [Sequence Asset](../../../../../The_Asset_Editors/Sequences) or [Sequence Object Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Sequence_Object_Struct)    | The sequence object struct or ID to get the objects from. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var _seq = sequence_get(seq_Logo);
obj_array = sequence_get_objects(_seq);
```

The above code gets the struct for a sequence object and then retrieves
the objects that it uses and stores the array in a variable.
