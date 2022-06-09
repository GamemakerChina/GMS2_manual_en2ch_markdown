# temp_directory

This can be used to return the temporary directory created for your game
each time it is run (the root does not contain the final "\\"). This
directory will hold files and can be accessed while the game is running,
but it will be removed (along with all files that it contains) when the
game is closed. **WARNING!** This function may not work as you expect
due to GameMaker being sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
temp_directory
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open(temp_directory + "\temp_ini.ini");
```

This will open an ini file in the temporary directory of the game
(creating it if it does not already exist).
