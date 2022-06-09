# texture_global_scale

This function allows you to control the scaling of the texture pages on
load from the WAD file that is part of your final game executable. The
input value must be a power of two value and will work such that:

-   To set the texture pages to be 1:1 use texture_global_scale(1)
-   To half textures all the time use texture_global_scale(2)
-   To quarter them use texture_global_scale(4) , etc...

In this way you can better control texture page memory usage on
platforms with low memory issues. Note that textures pages are created
on demand from the WAD, and so you can either call this at the start of
the game to load all textures scaled, or you can call it at specific
times to load specific textures, in which case you'd probably want to
call [ draw_texture_flush() ](draw_texture_flush) before calling
this function, then use the pre-fetch functions to get the correct
texture pages into memory.

#### Syntax:

``` gml
texture_global_scale(pow2integer);
```

|             |                                                                         |                                                                                |
|-------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Argument    | Type                                                                    | Description                                                                    |
| pow2integer |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The scale factor to use (1, no scale, 2, half scale, 4, quarter scale, etc...) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_texture_flush(); texture_global_scale(2);
 sprite_prefetch(spr_Trees);
```

The above code will flush all textures from memory, then set the texture
scaling to 2 (so texture pages are half size) and then finally pre-fetch
the texture page that the sprite "spr_Trees" is contained within.
