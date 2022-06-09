# Fonts

GameMaker has a number of functions that can be used to get information
about the included font assets, as well as a further set of functions
that can be used to change, add or remove fonts from your game at
run-time. In particular the function font_add() can be used to add
non-standard fonts, like Asian glyph fonts, from a \*.ttf or \*.otf
file. It is worth noting is that if you add a font to your game that
doesn't have the glyphs required by the text you wish to write, then the
Unicode character 9647 (▯) is used to substitute those missing glyphs
when rendering it in the draw event. So if your font doesn't have, for
example, the º symbol, then writing 90º will actually produce 90▯. The
following functions can be used to get information about font resources:

-   [font_get_name](font_get_name)
-   [font_get_fontname](font_get_fontname)
-   [font_get_first](font_get_first)
-   [font_get_last](font_get_last)
-   [font_get_italic](font_get_italic)
-   [font_get_bold](font_get_bold)
-   [font_get_size](font_get_size)
-   [font_get_texture](font_get_texture)
-   [font_get_uvs](font_get_uvs)
-   [font_get_info](font_get_info)

The following functions can be used to change and manipulate fonts
during a game:

-   [font_exists](font_exists)
-   [font_set_cache_size](font_set_cache_size)
-   [font_add_enable_aa](font_add_enable_aa)
-   [font_add_get_enable_aa](font_add_get_enable_aa)
-   [font_add](font_add)
-   [font_add_sprite](font_add_sprite)
-   [font_add_sprite_ext](font_add_sprite_ext)
-   [font_replace](font_replace)
-   [font_replace_sprite](font_replace_sprite)
-   [font_replace_sprite_ext](font_replace_sprite_ext)
-   [font_delete](font_delete)
-   [font_texture_page_size](font_texture_page_size)
