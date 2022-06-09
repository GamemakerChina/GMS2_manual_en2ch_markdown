# object_get_mask

This function will tell you whether the object you are checking has a
mask index or not, and if it does then it will return the index of that
mask (which is a sprite asset), or -1 if it does not. Please note that
this is not an instance function! You can have an object with no mask
while an instance of that same object can have one and vice-versa, or
they can even have different masks. You can set an individual instances
mask index using the [ mask_index
](../Sprites/Sprite_Instance_Variables/mask_index) instance
variable.

#### Syntax:

``` gml
object_get_mask(obj);
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
if (mask_index != object_get_mask(object_index))
{
    mask_index = object_get_mask(object_index);
}
```

The above example will check the mask index of the instance against the
mask of the object_index of the instance. If they are not the same, then
it will assign the same mask as the one the object index has to the
instance.
