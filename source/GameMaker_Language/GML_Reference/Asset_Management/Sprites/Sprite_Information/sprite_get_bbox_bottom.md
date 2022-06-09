# sprite_get_bbox_bottom

This function returns the relative position of the bottom of the sprite
bounding box. This value is given as a relative value based on the upper
left corner of the base sprite asset being (0,0). it is the same value
as can be found in the sprite editor for the [collision mask
properties](../../../../../The_Asset_Editors/Sprites) . The image
below shows how it is calculated:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Sprites/spr_bbox.png)  

#### Syntax:

``` gml
sprite_get_bbox_bottom(ind);
```

|          |                                                                   |                                   |
|----------|-------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                              | Description                       |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to check. |

#### Returns

``` gml
 Real
```

#### Example:

``` gml
var ww, hh; ww = sprite_get_bbox_left(sprite_index) - sprite_get_bbox_right(sprite_index); hh = sprite_get_bbox_bottom(sprite_index) - sprite_get_bbox_top(sprite_index);
```

The above code calculates the width and height of the collision mask
based on the relative bounding box side positions.
