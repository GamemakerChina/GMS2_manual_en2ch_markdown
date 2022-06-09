# working_directory

Working_directory can actually return two different values depending on
what you are using it for. If you are writing a file to disk,
working_directory points to the area of local storage that is reserved
for your game on the target device (in Windows this is "
%LOCALAPPDATA%/gamedir/ " where the "gamedir" is the directory with the
name of your game). However, when reading from disk, working_directory
can be *either* the local storage (
[game_save_id](../../General_Game_Control/game_save_id) ) *or* the
area where the [Included
Files](../../../../Settings/Included_Files#h) are stored. NOTE The
working_directory variable will return the path **including** the final
backslash. For example, if you have a default \*.txt file included with
your game and read it into memory using working_directory , then that
file will be taken from the area where the Included Files are stored. If
you then choose to write that information to a text file using
working_directory , this will write the file to the target platform's
local storage, where it will be read from the next time unless you
instruct GameMaker to delete the file, in which case working_directory
will once more point to the area where the Included Files are stored. It
is worth noting that *in general* you do not need to use this and simply
specify the file name itself (plus any additional path information),
which is sufficient. For example, this:

``` gml
file_text_open_read(working_directory + "my_file.txt");
```

would be better done as this:

``` gml
file_text_open_read("my_file.txt");
```

WARNING This function may not work as you expect due to GameMaker being
sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
working_directory
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open(working_directory + "temp_ini.ini");
```

This will open an ini file from the working directory of the game
(creating it if it does not already exist). This could be the local
storage, or the area where the included files are depending on whether
the file being looked for exists in either place.
