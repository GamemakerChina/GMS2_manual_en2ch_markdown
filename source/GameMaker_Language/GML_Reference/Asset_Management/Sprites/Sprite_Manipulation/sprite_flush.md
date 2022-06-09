# sprite_flush

With this function you can remove the given texture page for the given
sprite from texture memory. You supply the sprite index (as defined when
creating the sprite resource) and the texture page it is assigned to
will be removed from texture memory. Note that if the texture page is
used elsewhere in the room (by another instance sprite or a background,
etc...) you may get a minor performance hit as the page is immediately
reloaded, so care should be taken when using this function. Note that
the function will return -1 if flush is not supported for the chosen
resource, or it will return 0 if all worked correctly.

#### Syntax:

``` gml
sprite_flush(ind)
```

|          |                                                                   |                                                        |
|----------|-------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                              | Description                                            |
| ind      |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index (resource name) of the sprite asset to flush |

#### Returns:

``` gml
 Real

(-1 or 0)
```

#### Example:

``` gml
sprite_flush(spr_Player_Aura);
```

The above code flushes the sprite "spr_Player_Aura" from memory.
