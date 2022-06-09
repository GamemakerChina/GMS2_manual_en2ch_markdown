# font_get_name

This function can be used to get the name (as a string) that was given
to the font when it was added as an asset to the GameMaker Asset
Browser. Please note that this is *only* a string and cannot be used to
reference the font directly - for that you would need the *font index* .
You can, however, use this string to get the *font index* using the
returned string along with the function [ asset_get_index()
](../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
font_get_name(ind);
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
fnt_Name = font_get_name(font0);
```

The above code will get the name of a font resource as it appears in the
Asset Browser and store it as a string in the variable "fnt_Name".
