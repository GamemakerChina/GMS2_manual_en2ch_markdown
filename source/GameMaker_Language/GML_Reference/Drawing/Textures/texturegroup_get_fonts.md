# texturegroup_get_fonts

With this function you can retrieve the font index of each of the fonts
assigned to texture pages within the given texture group. You supply the
texture group ID string (as defined in the texture Group Editor) and the
function will return a 1D array where each entry contains the font index
for a font resource. If the function fails - ie: an invalid group is
given, or the group has no texture assigned to it - then the array will
be empty (0 length).

#### Syntax:

``` gml
texturegroup_get_fonts(tex_id);
```

|          |                                                                           |                                                   |
|----------|---------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                      | Description                                       |
| tex      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the texture group to check (a string) |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var _tex_array = texturegroup_get_fonts( "MainMenu");
for (var i = 0; i &amp;lt; array_length(_tex_array); ++i;)
{
    show_debug_message("Font " + string(i) + " Index:" + string(tex_array[i]));
}
```

The above code will retrieve the font indexes for the texture group
"MainMenu", then display those IDs in the console output window.
