# filename_path

Using this function returns the path part of the indicated file path,
including the final backslash.

#### Syntax:

``` gml
filename_path(fname);
```

|          |                                                                           |                                |
|----------|---------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                      | Description                    |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file name and path to use. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
path = filename_path(working_directory + "Test.ini");
```

The above code gets the path (as a string) of the specified file.
