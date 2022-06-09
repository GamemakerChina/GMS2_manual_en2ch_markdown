# sprite_get_tpe

This function will return a special value that relates to the position
of the given sprite and sub-image on the texture page used by your game.
In this way you can pass the value to extensions for use outside of the
compiled game, effectively bypassing the GameMaker drawing functions and
permitting the sprite to be used in DOM content which can then be drawn
anywhere within the window that contains the game canvas. This function
is of particular interest to those that wish to create buttons and other
interactive media outside of the GameMaker canvas element on their host
page using the function [ clickable_add()
](../../../Web_And_HTML5/clickable_add) . **NOTE** : This function
is for HTML5 only.

#### Syntax:

``` gml
sprite_get_tpe(sprite, index);
```

|          |                                                                            |                                                            |
|----------|----------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                |
| sprite   |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to find the texture page entry of. |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The image index of the sprite.                             |

#### Returns

``` gml
 Texture Page Entry
```

#### Example:

``` gml
home_but = clickable_add(32, 32, sprite_get_tpe(spr_MS_Home, 0), "http://macsweeney_games.com", "_blank", "width=700, height=500, menubar=0, toolbar=0, scrollbars=0");
```

The above code creates a DOM button at the position (32, 32) of the page
that the game canvas is running on. The button uses the sprite
referenced from the texture page as "spr_MS_Home" and when clicked the
button will open a new window for the specified URL and with the defined
properties for that window.
