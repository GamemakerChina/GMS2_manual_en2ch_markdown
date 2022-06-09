# clickable_exists

This function returns whether a clickable DOM icon has been created with
the specified index exists or not. Please note, that the value used for
checking *must have been initialised previously* or else you will get an
error causing GameMaker to close.

#### Syntax:

``` gml
clickable_exists(index);
```

|          |                                                                                                |                                      |
|----------|------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                           | Description                          |
| index    |  [Clickable ID](../../../../GameMaker_Language/GML_Reference/Web_And_HTML5/clickable_add)  | The index of the clickable to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !clickable_exists(home_but)
{
    home_but = clickable_add(32, 32, sprite_get_tpe(spr_MS_Home, 0), "http://macsweeney_games.com", "_blank", "width=700, height=500, menubar=0, toolbar=0, scrollbars=0");
}
```

The above code checks the variable "home_but" to see if it already
exists, and if it does not it creates a clickable DOM icon at the
position (32, 32) of the page that the game canvas is running on. The
icon uses the sprite referenced from the texture page as "spr_MS_Home"
and when clicked the icon will open a new window for the specified URL
and with the defined properties for that window.
