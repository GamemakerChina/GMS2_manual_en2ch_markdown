# in_sequence

This is a **built-in variable** that is part of the [instance
variables](../Instances/Instance_Variables/Instance_Variables)
created for every object instance in your game. If the instance is being
controlled by a sequence, this variable will return true , otherwise it
will return false . This is a **read-only** variable and cannot be
changed. Note that this variable will become false after the controlling
Sequence has ended, even if its Sequence Element still exists, and will
become true if that Sequence element is [played
again](../Rooms/Sequence_Layers/layer_sequence_play) . You can use
this variable in your player (or CPU) controlled objects to make sure
that they're only moved by code when they're not in a Sequence. This can
prove useful for cutscenes, when you need to use the same instances in a
Sequence (using the
[sequence_instance_override_object()](sequence_instance_override_object)
function) and you need to make sure that they can't be moved by their
usual code while that cutscene is active.

#### Syntax:

``` gml
in_sequence
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (!in_sequence) {
     x += move_x;     y += move_y; }
```

The above code checks the in_sequence variable, and if it is false
(meaning the instance is not being controlled by a sequence) then it
adds move_x and move_y to the instance's position, making sure that it
only moves when it's not in a Sequence.
