# Textures

The following functions are all related to "textures", ie: images that
are stored in VRAM to be used as sprites or other things within your
game. The first set of functions available are used to retrieve
information about specific images and their position or size on the
[Texture
Page](../../../../Settings/Texture_Information/Texture_Pages) , as
well as set certain texture features:

-   [texture_get_width](texture_get_width)
-   [texture_get_height](texture_get_width)
-   [texture_get_texel_width](texture_get_texel_width)
-   [texture_get_texel_height](texture_get_texel_height)
-   [texture_get_uvs](texture_get_uvs)
-   [texture_set_stage](texture_set_stage)
-   [texture_global_scale](texture_global_scale)

GameMaker also has a number of functions related to the managing the
VRAM associated with individual textures as well as whole texture
groups:

-   [draw_texture_flush](draw_texture_flush)
-   [texture_prefetch](texture_prefetch)
-   [texture_flush](texture_flush)
-   [sprite_flush](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_flush)
-   [sprite_flush_multi](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_flush_multi)
-   [sprite_prefetch](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_prefetch)
-   [sprite_prefetch_multi](../../Asset_Management/Sprites/Sprite_Manipulation/sprite_prefetch_multi)
-   [draw_flush](../draw_flush)

Finally, we have the following functions which are primarily for use to
debug the project and ensure efficient use of texture memory:

-   [texture_debug_messages](texture_debug_messages)
-   [texture_is_ready](texture_is_ready)
-   [texturegroup_get_textures](texturegroup_get_textures)
-   [texturegroup_get_sprites](texturegroup_get_sprites)
-   [texturegroup_get_fonts](texturegroup_get_fonts)
-   [texturegroup_get_tilesets](texturegroup_get_tilesets)
