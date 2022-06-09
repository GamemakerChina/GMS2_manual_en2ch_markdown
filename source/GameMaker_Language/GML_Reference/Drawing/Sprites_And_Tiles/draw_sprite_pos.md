# draw_sprite_pos

With this function you can draw a sprite distorted over the area defined
by the four corner coordinates. The first two arguments are the sprite
to draw and the sub-image of the sprite (the same as in the function [
draw_sprite() ](draw_sprite) ) but the next ones are those that
define the position of each of the four corners of the **bounding box**
of the given sprite. These should be given in *clockwise* order, so the
first coordinate is the top left, then the top right, then bottom right
and finally the bottom left. You can also set a value for the alpha of
the sprite to draw it with transparency. The image below illustrates how
this function works:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/draw_sprite_pos.png)  
**WARNING!** The image above is only for illustrative purposes, and if
you use this function on a sprite, you will get different results and
may experience texture "shearing" due to the way that a sprite is
constructed from a quad of primitives. **NOTE** : This function is only
useful for **bitmap** sprites and will not work with SWF or JSON (Spine)
sprites. **NOTE** : When using this function, you should have the
[Automatically Crop](../../../../Settings/Texture_Groups) setting
disabled for texture pages.

#### Syntax:

``` gml
draw_sprite_pos(sprite, subimg, x1, y1, x2, y2, x3, y3, x4, y4, alpha);
```

|          |                                                                         |                                                                                                                         |
|----------|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                                                             |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to draw.                                                                                        |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The subimg (frame) of the sprite to draw (image_index or -1 correlate to the current frame of animation in the object). |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The first x coordinate.                                                                                                 |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The first y coordinate.                                                                                                 |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The second x coordinate.                                                                                                |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The second y coordinate.                                                                                                |
| x3       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The third x coordinate.                                                                                                 |
| y3       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The third y coordinate.                                                                                                 |
| x4       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The fourth x coordinate.                                                                                                |
| y4       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The fourth y coordinate.                                                                                                |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The alpha of the sprite (from 0 to 1 where 0 is transparent and 1 opaque).                                              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_sprite_pos(sprite_index, image_index, x - 100, y - 50, x - 50, y +150, x + 100, y + 200, x + 100, y, 1);
```

The above code will draw the sprite associated with the instance running
the code distorted around the x / y position of the instance and with a
fully opaque alpha.
