# audio_emitter_create

This function creates a new audio emitter and returns the index for it.
This index should be stored in a variable for all further functions that
relate to this emitter, and then when it is no longer needed it should
be removed from memory using the function [ audio_emitter_free()
](audio_emitter_free) to prevent memory leaks which may eventually
crash your game.

#### Syntax:

``` gml
audio_emitter_create();
```

#### Returns:

``` gml
 Audio Emitter ID
```

#### Example:

``` gml
s_emit = audio_emitter_create();
```

The above code creates a new audio emitter and assigns its index to the
variable "s_emit".
