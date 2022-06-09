# audio_group_name

This function will return a string containing the name of the given
audio group for displaying or checking. When you define an audio group
in the Game Options, you give it a unique "name" which is really a
constant to use as an ID *v* alue for the group. All this function does
is take the ID and return a string of the ID name you gave.

#### Syntax:

``` gml
audio_group_name(groupID);
```

|          |                                                                                                                             |                                                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                                               |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index value constant of the audio group to check (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var name = audio_group_name(audiogroup_level1);
draw_text(32, 32, "Now Playing Group: " + name);
```

The above code retrieves the name of the given audio group constant and
displays it on the screen.
