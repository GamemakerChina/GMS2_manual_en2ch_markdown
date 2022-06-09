# sequence_instance

This is a **built-in variable** that is part of the [instance
variables](../Instances/Instance_Variables/Instance_Variables)
created for every object instance in your game. If the instance is being
controlled by a sequence, this variable will hold the [sequence instance
struct](Sequence_Structs/The_Sequence_Instance_Struct) for the
Sequence controlling the instance, otherwise it will be undefined . This
is a **read-only** variable and cannot be changed. Note that this
variable will become undefined after the controlling Sequence has
ended, even if its Sequence Element still exists, and will get the
struct again if that Sequence element is
[replayed](../Rooms/Sequence_Layers/layer_sequence_play) .

#### Syntax:

``` gml
sequence_instance
```

#### Returns:

``` gml
 Sequence Instance Struct
```

#### Example:

``` gml
if (in_sequence)
{
    sequence_instance.speedScale = 2;
}
```

The above code checks the [ in_sequence ](in_sequence) variable, and
if it is true (meaning the instance is being controlled by a sequence)
then it will change the speed scale of that Sequence to 2.
