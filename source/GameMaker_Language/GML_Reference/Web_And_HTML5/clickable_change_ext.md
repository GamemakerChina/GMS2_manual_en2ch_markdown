# clickable_change_ext

With this function you can change the sprite and position of a clickable
icon previously created with [ clickable_add() ](clickable_add) .
Bear in mind that the position is based on the window, *not* the canvas,
(0,0) position and that the sprite must be referenced directly from the
texture page (see: [ sprite_get_tpe()
](../Asset_Management/Sprites/Sprite_Information/sprite_get_tpe) ).
This function also permits you to change the scale of the sprite used
(as a multiplier so that 1 is the default, 0.5 would be half and 2 would
be double) and the alpha value from 0 (fully transparent) to 1 (fully
opaque) for the final icon on the screen.

#### Syntax:

``` gml
clickable_change_ext(index, tpe, x, y, alpha, scale)
```

|          |                                                                                                                                     |                                                  |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                | Description                                      |
| index    |  [Clickable ID](../../../../GameMaker_Language/GML_Reference/Web_And_HTML5/clickable_add)                                       | The index of the clickable icon to change.       |
| tpe      |  [Texture Page Entry](../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_tpe)  | The texture page entry for the sprite to be used |
| x        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The new x position within the *window* .         |
| y        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The new y position within the *window* .         |
| scale    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The scale of the icon (default 1).               |
| alpha    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The image alpha of the icon (default 1).         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
switch (room)
{
    case rm_Menu: clickable_change_ext(global.Help_Icon, sprite_get_tpe(spr_MS_Help, 1), 32, 32, 2, 1); break;
    case rm_Game: clickable_change_ext(global.Help_Icon, sprite_get_tpe(spr_MS_Help, 0), 200, 32, 1, 0.5); break;
}
```

The above code will change the image index and position of the clickable
icon indexed in the variable "global.Help" depending on the current
room, changing the icon scale and alpha too.
