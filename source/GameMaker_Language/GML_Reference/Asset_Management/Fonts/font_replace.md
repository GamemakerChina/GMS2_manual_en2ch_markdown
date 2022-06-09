# font_replace

This function can be used to replace a font in your game from those
fonts that are installed on the system it is running on. Note that the
font being replaces *cannot* be a font from the Asset Browser, and must
be a font that was added previously using the function [ font_add()
](font_add) . When replacing a font in this way, you can define the
size of the font (in points), as well as whether the font should be
**bold** or *italic* , and you can also define the range of characters
to include. If the function fails then it will fail silently and the
given font will not be replaced. For the HTML5 target module, this
function **can only be used to replace *Web Fonts*** , and will only
work if WebGL is **not** enabled - if WebGL is enabled then you must use
a general font resource (ie: using [ draw_set_font()
](../../Drawing/Text/draw_set_font) along with a font from the Asset
Browser) or bitmap fonts (see [ font_add_sprite() ](font_add_sprite)
). IMPORTANT When targeting HTML5, italics and bold text is only
supported if the font asset or web font itself has these characters
included. They will not be synthesised from the base font. The following
table shows the fonts that are standard across all browsers and that
should be be available for use without problems. Any other font may or
may not exist on the computer or device that is running your game, so
the use of this function should be limited to these standard fonts:

|                                  |                         |             |
|----------------------------------|-------------------------|-------------|
| Windows Font Name                | Mac Font Name           | Font Family |
| Arial                            | Arial / Helvetica       | sans-serif  |
| Arial Black                      | Arial Black / Gadget    | sans-serif  |
| Comic Sans MS                    | Comic Sans MS           | cursive     |
| Courier New                      | Courier New             | monospaced  |
| Georgia                          | Georgia                 | serif       |
| Impact                           | Impact / Charcoal       | sans-serif  |
| Lucida Console                   | Monaco                  | monospaced  |
| Lucida Sans Unicode              | Lucida Grande           | sans-serif  |
| Palatino Linotype / Book Antiqua | Palatino                | serif       |
| Tahoma                           | Geneva                  | sans-serif  |
| Times New Roman                  | Times New Roman / Times | serif       |
| Trebuchet MS                     | Trebuchet MS            | sans-serif  |
| Verdana                          | Verdana / Geneva        | sans-serif  |
| Georgia                          | Georgia                 | serif       |
| Symbol                           | Symbol                  | N/A         |
| Webdings                         | Webdings                | N/A         |
| Wingdings                        | Zapf Dingbats           | N/A         |
| MS Sans Serif                    | Geneva                  | sans-serif  |
| MS Serif                         | New York                | sans-serif  |

On all other (non Web) targets, you can use this function to replace a
font from a file. The file **must be included in the game bundle** using
the [Included Files](../../../../Settings/Included_Files)
functionality of GameMaker , and must be either a \*.ttf or \*.otf
format font file, useful for adding non-standard fonts like Asian or
Arabic. TIP If you include such a font file with a game, ensure that it
is **properly licensed** for distribution with the game. When loading a
font from a file in this way the *size* of the font is in **pixels** and
the *first* and *last* values are ignored, meaning all glyphs in the
font will be added. Fonts added in this way are assigned to their own
texture page, so care should be taken when using this function as it
will increment the number of texture swaps when drawing. It is also
worth noting that fonts may appear slightly larger when drawn, since
glyphs may have parts that are drawn outside of the bounding box defined
for the font. You should be aware too that there is a limitation of
around 200 glyphs that can be rendered in a single frame for a
particular font. ** NOTE ** When you load a font into GameMaker you must
remember to remove it again (with [ font_delete() ](font_delete) )
when no longer needed, otherwise there is risk of a memory leak which
will slow down and eventually crash your game.

#### Syntax:

``` gml
font_replace(ind, name, size, bold, italic, first, last);
```

|          |                                                                            |                                                                                                                         |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                                                             |
| ind      |  [Font Asset](../../../../../The_Asset_Editors/Fonts)                  | The index of the (previously added) font to be replaced.                                                                |
| name     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)   | The name of the font to be used (eg 'Arial'), or the file path if the font is an included \*. ttf or \*.otf file.       |
| size     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The size of the font - points for Web Fonts, pixels for file fonts.                                                     |
| bold     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the font is bold (true) or not (false).                                                                         |
| italics  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the font is italic (true) or not (false).                                                                       |
| first    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The first character to include (if you're unsure, go for 32).                                                           |
| last     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The last character to include (if you're unsure, go for 128).                                                           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
font_replace(myfont, "Arial", 24, true, true, 32, 128);
```

This will replace the font indexed in the variable "myfont" with a new
font that is 24pt in size, uses "Arial" and which is bold and italic.
The font range includes capital and lower case letters, numbers and all
common punctuation.
