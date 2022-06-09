# sprite_prefetch_multi

This function can be used to prefetch (place into texture memory) a
number of texture pages that contain the sprites given. You supply an
array populated with the sprite indices (as defined when you created the
sprite asset) and the texture pages that they are on will be loaded into
memory. Note that the function will return -1 if prefetch is not
supported for the chosen resource or the target platform is HTML5, or it
will return 0 if all worked correctly. **NOTE** : There is a performance
hit as the texture is uploaded to texture memory on most devices, so
it's recommended that you call sprite_prefetch_multi() on any required
graphics at the start of a level to avoid any stalls.

#### Syntax:

``` gml
sprite_prefetch_multi
```

|          |                                                                                                                                                |                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                                           | Description                            |
| array    |  [Array](../../../../../../GameMaker_Language/GML_Overview/Arrays) of [Sprite Asset](../../../../../../The_Asset_Editors/Sprites) s    | Array with the sprite indices to fetch |

#### Returns:

``` gml
 Real

(-1 or 0)
```

#### Example:

``` gml
spr_a[0] = spr_Player_Aura1;
spr_a[1] = spr_Player_Aura2;
spr_a[2] = spr_Player_Aura3;
spr_a[3] = spr_Player_Aura4;
sprite_prefetch_multi(spr_a);
```

The above code creates an array where each element holds a sprite index.
This array is then used to place those sprite textures into memory.
