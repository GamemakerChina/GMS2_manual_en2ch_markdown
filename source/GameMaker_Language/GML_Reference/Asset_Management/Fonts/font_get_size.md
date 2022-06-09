# font_get_size

With this function you can get the size of any font resource, which is
the point value shown by the font resource dialogue.

#### Syntax:

``` gml
font_get_size(ind);
```

|          |                                                            |                                       |
|----------|------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                       | Description                           |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | Index of the font to get the size of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
sz = font_get_size(font0);
```

This will get the size of the font indexed by the "font0" variable and
store it in the variable "sz".
