# sprite_replace

This function works in almost the exact same manner as [ sprite_add()
](sprite_add) , only instead of returning the index of the sprite
you are importing, it overwrites a previously created sprite index. When
using this function you should use a sprite index that has been created
and stored in a variable using other functions like [ sprite_add()
](sprite_add) or [ sprite_create_from_surface()
](sprite_create_from_surface) , or even [ sprite_duplicate()
](sprite_duplicate) , rather than a resource tree sprite asset. You
*can* replace a sprite from the game assets using this function, but
doing so means that you will lose the reference ID for the sprite that
you are replacing, regardless of whether you call game_restart() or not,
and so is not recommended. Regardless of the sprite being replaced, this
function will **create a new texture page for the sprite** and so care
should be taken when using it as it may adversely affect performance by
increasing the number of required texture swaps for rendering. The image
file to be loaded should **always** be in \*.png format and all images
that are to be turned into animated sprites should have a "strip" format
(see the image below). They will be split into the number of sub-images
specified following the rule **sprite width = strip width / sub images**
.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Sprites/spr_strip.png)  
As you can see in the above image, the sprite has been placed on a dark
purple background, and this can be removed by setting the "removeback"
argument to true . This works by checking the *bottom left* pixel of the
sprite for the colour there and then uses that as the colour to be
removed. For example, in the above image, if we had the bottom left
pixel colour as green, all the green parts of the sprite would have been
removed and the rest of the purple background ignored. If you choose the
"removeback" option, you may also want GameMaker to smooth the edges of
the sprite by setting the "smooth" argument to true . All this does is
create a semi-transparent border around the edges of the sprite after it
has had its background removed. Finally you can also specify the x and y
*origin* for the sprite. This is the point where the sprite is "fixed"
onto the instance that uses it, and is always calculated as relative to
the 0,0 top left corner of one sprite sub-image. So, for example, a
sprite that is 32 x 32 pixels with these values set to (16,16) will have
its origin in the center. By default all new sprites have their bounding
boxes calculated automatically (the exact bbox will depend on the size
and transparency of the sprite), however you may wish to customise this,
in which case you should also use the function [ sprite_collision_mask()
](sprite_collision_mask) . **NOTE** : Depending on the target
platform that is chosen you are limited as to where you can save and
load files from. See [File
Handling](../../../../../Additional_Information/The_File_System) for
more information. **NOTE** : You should be aware that if you are using
this function in your HTML5 target game to load resources from an
external server, then, due to XSS protection in browsers, attempts to
load resources from across domains can be blocked and may appear to
return blank results.

#### Syntax:

``` gml
sprite_replace(ind, fname, imgnumb, removeback, smooth, xorig, yorig);
```

|            |                                                                               |                                                                                                            |
|------------|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Argument   | Type                                                                          | Description                                                                                                |
| ind        |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)              | The index of the sprite to permanently replace.                                                            |
| fname      |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)   | The filename of the image to make the new sprite.                                                          |
| imgnumb    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The number of frames the sprite will be cut up into horizontally. Use 1 for one single image or \*.gif .   |
| removeback |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Indicates whether to make all pixels with the background colour (left-bottom pixel) transparent.           |
| smooth     |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Indicates whether to smooth the edges.                                                                     |
| xorig      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of the origin, relative to the sprite's top left corner.                                  |
| yorig      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of the origin, relative to the sprite's top left corner.                                  |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
sprite_replace(spr_banner, "gravemaker.png", 1, false, false, 0, 0);
```

The above code will replace the image asset indexed in "spr_banner" with
another one loaded from an external source.
