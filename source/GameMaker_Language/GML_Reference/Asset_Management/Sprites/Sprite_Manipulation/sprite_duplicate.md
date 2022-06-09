# sprite_duplicate

This function will return the index of a newly created sprite that is a
duplicate (copy) of the one input as the "index" argument. If the
function fails, -1 is returned. This function *must* be used to copy any
sprites from the original assets before any transformations can be done
on them. For example, if you wish to change the bounding box for a
sprite, or set its alpha from another sprite, you must first duplicate
it, then perform the operation on the duplicated sprite and use that. A
duplicated sprite will be places on its own unique texture page when
created, meaning that duplicating multiple sprites will create multiple
texture pages and have an impact on performance, so use this function
only when necessary. **NOTE** : When you duplicate a sprite in GameMaker
you must remember to remove it again (with [ sprite_delete()
](sprite_delete) ) when no longer needed, otherwise there is risk of
a memory leak which will slow down and eventually crash your game.

#### Syntax:

``` gml
sprite_duplicate(index);
```

|          |                                                                   |                                       |
|----------|-------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                              | Description                           |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to duplicate. |

#### Returns

``` gml
 Sprite Asset

or -1
```

#### Example:

``` gml
new_spr = sprite_duplicate(sprite_index)
```

The above code duplicates the sprite currently being used as the sprite
index of the instance and stores the index for this new sprite in the
variable "new_spr".
