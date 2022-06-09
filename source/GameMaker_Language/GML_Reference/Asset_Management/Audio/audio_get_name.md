# audio_get_name

This function will return the name of a given audio resource as a
string. The "index" value can be that of the resource itself (as seen in
the Asset Browser) or the unique ID value that is given when you play
the sound using, for example, [ audio_play_sound()
](audio_play_sound) . Note that the string returned is *not* the
same as the resource ID and cannot be used to access the resource
itself, so should only be used for displaying or error checking.

#### Syntax:

``` gml
audio_get_name(index);
```

|          |                                                              |                                  |
|----------|--------------------------------------------------------------|----------------------------------|
| Argument | Type                                                         | Description                      |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)  | The index of the sound to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var snd = audio_play_sound(choose(snd_One, snd_Two, snd_Three), 0, false); var name = audio_get_name(snd); show_debug_message("Sound = " + name);
```

The above code plays a random sound chosen from three different sound
resources then shows a debug message with its name.
