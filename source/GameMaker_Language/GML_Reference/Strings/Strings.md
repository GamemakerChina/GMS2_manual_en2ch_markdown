# Strings

At some time when making your game you will need to use text. Text in
games is dealt with by using the **string** functions (a string is just
another way of saying a line of text) and GameMaker has a complete set
of functions that permit you to manipulate strings in many ways,
including the insertion of one string in another, the copying of strings
and the ability to parse strings for the digits or the letters that they
contain. In general a string can *only* be created by adding text within
double quotes " " and *single quote strings are not accepted* , nor can
you split the string over multiple lines and expect GameMaker to render
it as if the line breaks were newlines (unless a **string literal** @
identifier is used, as explained below). It is worth noting that there
are certain conventions that you can use when creating strings, mostly
concerned with using *escape characters* . These are characters that are
preceded by a " \\ " symbol. So, for example, if you wanted to put
quotation marks within a string you would have something like this:

``` gml
str = "Hello\"World\"";
```

GameMaker also has full four byte wide Unicode character support,
allowing you to decode and encode Unicode characters in the upper bounds
of the standard (including - but not limited to - emoji). To deal with
Unicode characters, you can use the " \\ " to precede any Unicode
literal - digits of hex preceded a " u ", for example " \u00e2 " for
"á"- where the digits are the number of the Unicode character. When
working with Unicode in this way, you need to be aware of the fact that
GameMaker will interpret *all* digits following the " u ", so if you
wanted to write "áa" for example, you should use:

``` gml
"\u00e2\a"
```

or

``` gml
"\u00e2\u61"
```

or

``` gml
"\u00e2" + "a"
```

as just using " \u00e2a " would actually result in the Unicode character
" ส " (essentially becoming " \ue2a "). GameMaker can also handle any
hexadecimal literal - normally written as digits of hex following " 0x
", for example " 0xff ", where the digits are the number of the
character to use. In GameMaker these are written using " \x " and then
the hex value. These and other predefined escape characters are listed
in the table below:

|                    |                                |
|--------------------|--------------------------------|
| Constant           | Description                    |
| \n                 | Newline                        |
| \r                 | Carriage return                |
| \b                 | Backspace (0x08)               |
| \f                 | Form Feed (0x0c)               |
| \t                 | Horizontal Tab (0x09)          |
| \v                 | Vertical Tab (0x0b)            |
| \\\\               | Backslash itself (0x5c)        |
| \a                 | Alert (0x07)                   |
| \u\[Hex Digits\]   | Insert Unicode character       |
| \x\[Hex Digits\]   | Insert hex literal character   |
| \\\[Octal Digits\] | Insert octal Unicode character |

**NOTE** : Strings support form feed, vertical tab etc... but this does
not mean to say that **rendering** does, and when drawing strings these
characters may be ignored. You can also create verbatim *string
literals* by preceding the whole string with the @ character:

``` gml
var test = @"
Line breaks
over multiple
lines
";
```

The above code will render the string over multiple lines as if there
was a line break escape character included. A verbatim string literal is
similar to previous GameMaker version string literals but they also use
double or single quotes and must be prefixed by an @ symbol, they can be
broken over multiple lines in the code file and they DO NOT support
escaped characters i.e. @"Hello\World" will *not* try to escape the W on
World and will be stored verbatim. Note though that when using string
literals like this, you will need to break the string if you wish to
include quotation marks as part of the string, ie:

``` gml
var test = @"Hello " + "\"" + @"World" + "\""
```

Another thing to note is that the Unicode character 9647 (▯) is used to
substitute any missing glyphs that you may have in your designated font
when rendering it in the draw event. So if your font doesn't have, for
example, the ° symbol, then writing 90° will actually produce 90▯. The
following list of functions are all for dealing with strings:

-   [ansi_char](ansi_char)
-   [chr](chr)
-   [ord](ord)
-   [real](real)
-   [string](string)
-   [string_byte_at](string_byte_at)
-   [string_byte_length](string_byte_length)
-   [string_set_byte_at](string_set_byte_at)
-   [string_char_at](string_char_at)
-   [string_ord_at](string_ord_at)
-   [string_copy](string_copy)
-   [string_count](string_count)
-   [string_delete](string_delete)
-   [string_digits](string_digits)
-   [string_format](string_format)
-   [string_insert](string_insert)
-   [string_length](string_length)
-   [string_letters](string_letters)
-   [string_lettersdigits](string_lettersdigits)
-   [string_lower](string_lower)
-   [string_pos](string_pos)
-   [string_pos_ext](string_pos_ext)
-   [string_last_pos](string_last_pos)
-   [string_last_pos_ext](string_last_pos_ext)
-   [string_repeat](string_repeat)
-   [string_replace](string_replace)
-   [string_replace_all](string_replace_all)
-   [string_upper](string_upper)
-   [string_height](string_height)
-   [string_height_ext](string_height_ext)
-   [string_width](string_width)
-   [string_width_ext](string_width_ext)
-   [string_hash_to_newline](string_hash_to_newline)
-   [is_string](../Variable_Functions/is_string)

Other than those functions that relate specifically to strings, some
targets also give you access to the clipboard to get and set text
information:

-   [clipboard_has_text](clipboard_has_text)
-   [clipboard_get_text](clipboard_get_text)
-   [clipboard_set_text](clipboard_set_text)
