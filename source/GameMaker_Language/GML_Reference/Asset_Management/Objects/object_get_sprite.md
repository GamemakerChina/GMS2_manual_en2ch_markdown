# object_get_sprite

This function will tell you whether the object you are checking has a
sprite or not, and if it does then it will return the index of that
sprite, or -1 if it does not. Please note that this is not an instance
function! You can have an object with no sprite while an instance of
that same object can have one and vice-versa, or they can even have
different sprites. You can set an individual instances sprite using the
[ sprite_index ](../Sprites/Sprite_Instance_Variables/sprite_index)
instance variable.

#### Syntax:

``` gml
object_get_sprite(obj);
```

|          |                                                                |                                  |
|----------|----------------------------------------------------------------|----------------------------------|
| Argument | Type                                                           | Description                      |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The index of the object to check |

#### Returns:

``` gml
 Sprite Asset
```

#### Example:

``` gml
var _spr = object_get_sprite(object_index);
if (sprite_index != _spr)
{
    sprite_index = _spr;
}
```

The above example will check the sprite_index of the instance against
the sprite of the object_index of the instance. If they are not the
same, then it will assign the same sprite as that of the object index to
the instance.
