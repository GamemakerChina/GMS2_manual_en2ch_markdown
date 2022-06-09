# font_get_italic

With this function you can check any font asset to see if it has the
*italic* flag or not. If it does the function will return true ,
otherwise it will return false .

#### Syntax:

``` gml
font_get_italic(ind);
```

|          |                                                            |                             |
|----------|------------------------------------------------------------|-----------------------------|
| Argument | Type                                                       | Description                 |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | Index of the font to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if font_get_italic(fnt_Main)
{
    draw_set_font(fnt_Main);
}
```

This will set the active drawing font to fnt_Main if it is set as italic
in its font properties.
