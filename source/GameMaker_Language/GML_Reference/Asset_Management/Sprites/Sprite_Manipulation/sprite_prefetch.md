# sprite_prefetch

This function can be used to prefetch (place into texture memory) a
texture page with the given sprite. You supply the sprite index as
defined when you created the sprite asset, and the texture page it is on
will be loaded into memory. Note that the function will return -1 if
prefetch is not supported for the chosen resource or the target platform
is HTML5, or it will return 0 if all worked correctly. **NOTE** : There
is a performance hit as the texture is uploaded to texture memory on
most devices, so it's recommended that you call sprite_prefetch on any
required graphics at the start of a level to avoid any stalls.

#### Syntax:

``` gml
sprite_prefetch(ind)
```

|          |                                                                   |                           |
|----------|-------------------------------------------------------------------|---------------------------|
| Argument | Type                                                              | Description               |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The sprite index to fetch |

#### Returns:

``` gml
 Real

(-1 or 0)
```

#### Example:

``` gml
sprite_prefetch(spr_Player_Aura);
```

The above code will place the referenced sprite into texture memory
ready for use.
