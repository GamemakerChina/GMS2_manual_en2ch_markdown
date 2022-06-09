# sequence_create

With this function you can create a new sequence object which you can
then add tracks to. The function returns a
[struct](../../../GML_Overview/Structs) which you can then access to
setup the new sequence you have created. The contents of this struct are
detailed on [this page](Sequence_Structs/The_Sequence_Object_Struct)
. The sequence object struct can then be used to create instances of the
sequence on a room layer using the function [ layer_sequence_create()
](../Rooms/Sequence_Layers/layer_sequence_create) . Note that when
creating sequence objects in this way you should remove them again by
calling the function [ sequence_destroy() ](sequence_destroy) when
they are no longer required, otherwise you will have a memory leak which
can slow down and eventually crash your game.

#### Syntax:

``` gml
sequence_create();
```

#### Returns:

``` gml
 Sequence Object Struct
```

#### Example:

``` gml
myseq = sequence_create();
myseq.length = 120;
myseq.loopmode = seqplay_pingpong;
```

The above code creates a new sequence object struct and sets its
playback length and loop mode.
