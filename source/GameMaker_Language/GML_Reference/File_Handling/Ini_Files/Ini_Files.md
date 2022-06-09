# Ini Files

INI files are small, lightweight files which are compatible with most
platforms. They are ideal for storing *small* pieces of information,
like interface preferences, local high scores, level data etc... and as
such are a great and easy way for you to start saving information from
your games. However, it is worth noting that they do have a limit on the
data they can store, which is a maximum of 64KB, so if you are saving
things like Data Structures, you may wish to look at some of the other
file functions like [Text Files](../Text_Files/Text_Files) .
**IMPORTANT!** All GameMaker projects have a file called " options.ini
", so you **cannot** name any file with that name (you will get a uid
failure when you try to compile your game project). Please note that for
games with localizations it is very important that accented letters can
be read from external files. This means that you should create the ini
file in **UTF8** format *first* and then add it into GameMaker as an
included file so that it is exported on running the game and used
instead of the default ANSI format ini file that is created by the ini
functions when none has been previously supplied. In this way, you can
read and write to it correctly with all accents and non-Roman letters
being maintained. The following functions exist for ini files:

-   [ini_open](ini_open)
-   [ini_close](ini_close)
-   [ini_write_real](ini_write_real)
-   [ini_write_string](ini_write_string)
-   [ini_read_real](ini_read_real)
-   [ini_read_string](ini_read_string)
-   [ini_key_exists](ini_key_exists)
-   [ini_section_exists](ini_section_exists)
-   [ini_key_delete](ini_key_delete)
-   [ini_section_delete](ini_section_delete)
-   [ini_open_from_string](ini_open_from_string)
