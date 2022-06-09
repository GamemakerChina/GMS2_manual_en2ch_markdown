# program_directory

This will return the directory where the game executable is stored.
However this may not always be useful, particularly as some devices run
the exe from a \*.zip file, so this would return the same no matter
where the game is actually running from. **WARNING!** This function may
not work as you expect due to GameMaker being sandboxed! Please see the
section on the [File
System](../../../../Additional_Information/The_File_System) for more
information. **NOTE** : If you disable the sandbox then you still will
not be able to write to this directory to prevent any possible issue
with deleting required game files.

#### Syntax:

``` gml
program_directory
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
dir = program_directory;
```

This will store the directory where the executable is stored in a
variable.
