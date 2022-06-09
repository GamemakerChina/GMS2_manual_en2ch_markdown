# font_delete

With this function you can delete a font asset from the game. This is a
**permanent** removal, and changing rooms, or restarting the game will
not bring the removed font back. For that the player would need to exit
the game and restart that way, so take care when using this function. In
general it is only needed for freeing up memory that has been used by a
font added to the game through the functions [ font_add()
](font_add) or [ font_add_sprite() ](font_add_sprite) .

#### Syntax:

``` gml
font_delete(ind);
```

|          |                                                            |                                  |
|----------|------------------------------------------------------------|----------------------------------|
| Argument | Type                                                       | Description                      |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)  | The index of the font to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
font_delete(global.Font);
```

The above code will delete the font indexed in the global variable
"Font".
