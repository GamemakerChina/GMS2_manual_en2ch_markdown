# sprite_flush_multi

With this function you can remove the any number of texture pages for
the given sprites from texture memory. You supply the sprite indices as
an array and the texture pages they are assigned to will be removed from
texture memory. Note that if one of the texture pages is used elsewhere
in the room (by another instance sprite or a background, etc...) you may
get a minor performance hit as the page is immediately reloaded back
into memory again, so care should be taken when using this function.
Note that the function will return -1 if flush is not supported for the
chosen resources, or it will return 0 if all worked correctly.

#### Syntax:

``` gml
sprite_flush_multi(array);
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| array    |  [Array](../../../../../../GameMaker_Language/GML_Overview/Arrays)  | Array with the sprite indices to flush |

#### Returns:

``` gml
 Real

(-1 or 0)
```

#### Example:

``` gml
spr_a[0] = spr_Player_Aura1; spr_a[1] = spr_Player_Aura2; spr_a[2] = spr_Player_Aura3; spr_a[3] = spr_Player_Aura4; sprite_flush_multi(spr_a);
```

The above code creates an array where each element holds a sprite index.
This array is then used to clear those sprite textures from memory.
