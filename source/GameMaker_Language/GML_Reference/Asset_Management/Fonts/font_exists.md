# font_exists

This function returns whether a font with the specified index exists or
not. You can check font indices as defined from the Asset Browser, or
fonts that have been added using functions like font_add() .

#### Syntax:

``` gml
font_exists(ind);
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
if font_exists(fnt_Main)
{
    draw_set_font(fnt_Main);
}
```

This will set the active drawing font to fnt_Main if it exists.
