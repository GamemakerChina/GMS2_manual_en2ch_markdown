# Text Files

Text files are a useful way to store large amounts of data externally
from your game. Contrary to ini files, you can have up to 32 text files
open at once, and you can read and write large chunks of data to them as
well. However, it is up to you to decide how that data should be
structured as there is no set "section" or "key" structure like with [
\*.ini files](../Ini_Files/Ini_Files) . Please note that for games
with localizations it is very important that accented letters can be
read from external files. This means that you should create the txt file
in **UTF8** format *first* and then add it into GameMaker as an included
file so that it is exported on running the game and used instead of the
default ANSI format txt file that is created by the GameMaker file
functions when no file is previously supplied. In this way, you can read
and write to it correctly with all accents and non-roman letters being
maintained. The following functions exist that deal with files:

-   [file_text_open_read](file_text_open_read)
-   [file_text_open_write](file_text_open_write)
-   [file_text_open_append](file_text_open_append)
-   [file_text_open_from_string](file_text_open_from_string)
-   [file_text_read_real](file_text_read_real)
-   [file_text_read_string](file_text_read_string)
-   [file_text_readln](file_text_readln)
-   [file_text_write_real](file_text_write_real)
-   [file_text_write_string](file_text_write_string)
-   [file_text_writeln](file_text_writeln)
-   [file_text_eoln](file_text_eoln)
-   [file_text_eof](file_text_eof)
-   [file_text_close](file_text_close)
