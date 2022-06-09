# sprite_assign

This function takes two previously created (or included) sprite indexes,
and copies the image from one to the other. In this way you can copy (or
"clone") one sprite into another index. Note that *you cannot copy to a
game resource* . You have to have created the sprite to be copied to
previously using the [ sprite_add() ](sprite_add) or [
sprite_duplicate() ](sprite_duplicate) functions.

#### Syntax:

``` gml
sprite_assign(index, sprite);
```

|          |                                                                   |                                                            |
|----------|-------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                              | Description                                                |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to be copied to (ie: overwritten). |
| sprite   |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The sprite to be copied from.                              |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
if sprite_exists(global.Player_Sprite)
{
    var t_spr = sprite_add("player.png", 16, true, true, 0, 0);
    sprite_assign(global.Player_Sprite, t_spr);
    sprite_delete(t_spr);
}
else
{
    global.Player_Sprite = sprite_add("player.png", 16, true, true, 0, 0);
}
```

The above code checks to see if the global variable "Player_Sprite"
contains a sprite and if it does it uses sprite_assign to change it for
one that has been loaded from an external file. If it does not contain a
sprite one is loaded and its index is stored in that variable.
