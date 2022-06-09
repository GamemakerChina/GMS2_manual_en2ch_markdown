# filename_ext

This function returns the extension part of the indicated file name,
including the leading dot.

#### Syntax:

``` gml
filename_ext(fname);
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
ext = filename_ext(file_find_first("*.*", 0));
```

The above code gets the extension (as a string) of the specified file.
