# sprite_set_cache_size_ext

When performing image blending, HTML5 cannot do it dynamically in the
same way an executable could be performed. Therefore GameMaker has to
temporarily save a blended copy of the image and load it in. This
function sets how many blended copies of the given sprite can be cached
before old ones are overwritten. Default is 4. This is applied to one
single given sub-image of the sprite.

#### Syntax:

``` gml
sprite_set_cache_size_ext(ind, index, max);
```

|          |                                                                            |                                                                       |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                           |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)           | The index of the sprite to change the cache size of.                  |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The sub-image of ind to change the cache size of.                     |
| max      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum number of cached copies of the sprite that can be stored. |

#### Returns

``` gml
N/A
```

#### Example:

``` gml
sprite_set_cache_size_ext(sprite0, 0, 2);
```

This will set the sprite cache of the first sub-image of sprite0 to 2
copies.
