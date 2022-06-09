# audio_get_type

When adding audio to GameMaker it can be either *streamed* or *in
memory* . If you need to know whether a given sound index is for
streamed audio or not you can use this function which will return 1 for
streamed, 0 for sound in memory, and -1 if there is any error or the
index does not point to a valid sound resource.

#### Syntax:

``` gml
audio_get_type(index);
```

|          |                                                              |                                  |
|----------|--------------------------------------------------------------|----------------------------------|
| Argument | Type                                                         | Description                      |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)  | The index of the sound to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
type = audio_get_type(snd_Music_1);
```

The above code checks the type of audio indexed in the variable
"snd_Music_1" and stores the returned value in the variable "type".
