# audio_free_buffer_sound

With this function you can free up the pointer index value associated
with the sound ID. Freed sounds will not be available for playing, and
if multiple instances of the sound are being played they will all be
stopped. Note that before you can delete the buffer itself, you must
first free all sound ID's associated with it.

#### Syntax:

``` gml
audio_free_buffer_sound(index);
```

|          |                                                                 |                                          |
|----------|-----------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                            | Description                              |
| index    |  [Sound Asset](../../../../../../The_Asset_Editors/Sounds)  | The index of the buffered sound to free. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
audio_free_buffer_sound(soundID);
```

The above code frees the buffered sound indexed in the variable
"soundID".
