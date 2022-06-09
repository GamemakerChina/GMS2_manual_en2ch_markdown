# font_set_cache_size

When performing image blending and colouring, HTML5 cannot do it
dynamically in the same way an executable could be performed. Therefore
GameMaker has to temporarily save a blended copy of the images and load
them in when needed. This function sets how many blended copies of the
given font can be cached before old ones are overwritten. The default
value is 4. ** NOTE ** for sprite fonts you should be using the
equivalent function for sprites, [ sprite_set_cache_size()
](../Sprites/Sprite_Manipulation/sprite_set_cache_size) .

#### Syntax:

``` gml
font_set_cache_size(ind, max);
```

|          |                                                                         |                                                                     |
|----------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                         |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)               | The index of the font to change the cache size of.                  |
| max      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum number of cached copies of the font that can be stored. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
font_set_cache_size(fnt_MainMenu, 2);
```

This will set the font cache of the font indexed in the variable
"fnt_MainMenu" to 2 copies.
