# filename_drive

This function returns the drive information of the filename.

#### Syntax:

``` gml
filename_drive(fname);
```

|          |                                                                           |                  |
|----------|---------------------------------------------------------------------------|------------------|
| Argument | Type                                                                      | Description      |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file to use. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
drive = filename_drive(file_find_first(working_directory + "*.doc", 0));
```

The above code gets the drive information (as a string) of the specified
file.
