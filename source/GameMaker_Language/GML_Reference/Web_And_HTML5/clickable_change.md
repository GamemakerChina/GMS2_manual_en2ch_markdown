# clickable_change

With this function you can change the sprite and position of a clickable
icon previously created with [ clickable_add() ](clickable_add) .
Please note that the position is based on the window, *not* the canvas,
(0,0) position and that the sprite must be referenced directly from the
texture page (see: [ sprite_get_tpe()
](../Asset_Management/Sprites/Sprite_Information/sprite_get_tpe) ).

#### Syntax:

``` gml
clickable_change(index, tpe, x, y)
```

|          |                                                                                                                                     |                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                                                                                | Description                                       |
| index    |  [Clickable ID](../../../../GameMaker_Language/GML_Reference/Web_And_HTML5/clickable_add)                                       | The index of the clickable icon to change.        |
| tpe      |  [Texture Page Entry](../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_tpe)  | The texture page entry for the sprite to be used. |
| x        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The new x position within the *window* .          |
| y        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The new y position within the *window* .          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
switch (room)
{
    case rm_Menu: clickable_change(global.Help_Icon, sprite_get_tpe(spr_MS_Help, 1), 32, 32); break;
    case rm_Game: clickable_change(global.Help_Icon, sprite_get_tpe(spr_MS_Help, 0), 200, 32); break;
}
```

The above code will change the image index and position of the clickable
icon indexed in the variable "global.Help" depending on the current
room.
