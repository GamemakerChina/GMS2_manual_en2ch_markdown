# sequence_instance_override_object

With this function you can override (replace) all instances of an object
used in a sequence with another one. You supply the sequence instance
struct ID (as returned when the sequence instance was created in the
room or by using one of the room layer functions - see
[here](../Rooms/Sequence_Layers/Sequence_Layers) ), as well as the
object index (as defined in the asset browser) for the object that you
want to override. Finally you give an object index or an instance ID to
use as the object that is going to override the sequence (supplying an
instance ID will simply use the object that the instance was created
from as the override). Note that this can only be done on sequence
instances (not sequence objects) and must be done before the sequence
starts to play, otherwise it won't work.

#### Syntax:

``` gml
sequence_instance_override_object(sequence_instance_struct, object_id, instance_or_object_id);
```

|                          |                                                                                                                                                                                         |                                                                          |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument                 | Type                                                                                                                                                                                    | Description                                                              |
| sequence_instance_struct |  [Sequence Instance Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Sequence_Instance_Struct)                               | The sequence instance struct to modify.                                  |
| object_id                |  [Object Asset](../../../../../The_Asset_Editors/Objects)                                                                                                                           | The object index of the object within the sequence to override.          |
| instance_or_object_id    |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object index or instance ID to use to override the sequence objects. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _seq = layer_sequence_create("Background", 0, 0, seq_AnimatedBackground);
var _seq_inst = layer_sequence_get_instance(_seq);
sequence_instance_override_object(_seq_inst, obj_Trees_Winter, obj_Trees_Summer);
```

The above code creates a new sequence instance on the given layer and
then modifies it so that all instances of the object "obj_Trees_Winter"
are replaced by instances of the object "obj_Trees_Summer".
