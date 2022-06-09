# filename_dir

This function returns the directory part of the indicated file name,
which normally is the same as the path except for the final backslash.

#### Syntax:

``` gml
filename_dir(fname);
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
dir = filename_dir("Test.ini");
```

The above code gets the directory (as a string) of the specified file.
