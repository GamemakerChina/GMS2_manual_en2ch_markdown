# font_get_fontname

With this function you can get the actual system name of the given font
asset. This function returns a *string* and not an *index* , and the
name returned will depend on the font being used. For example, you may
have a font asset called " **fnt_Main** " in the Asset Browser, and the
font itself may be the Windows system font **Arial** . In this case the
function will return "Arial" as that is the system name of the font. If
you need the name that appears in the Asset Browser, use [
font_get_name() ](font_get_name) . The behaviour described above
only applies to font assets added through the IDE. When used on a font
loaded at runtime (using [font_add()](font_add) ), the function will
return the full path to that font file instead of its font name.

#### Syntax:

``` gml
font_get_fontname(ind);
```

|          |                                                            |                             |
|----------|------------------------------------------------------------|-----------------------------|
| Argument | Type                                                       | Description                 |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | Index of the font to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
fnt_Name = font_get_fontname(font0);
```

The above code will get the system name of a font resource and store it
as a string in the variable "fnt_Name".
