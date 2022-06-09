# filename_change_ext

This function returns the indicated file name with the extension
(including the dot) changed to the new extension. By using an empty
string as the new extension you can remove the extension part all
together.

#### Syntax:

``` gml
filename_change_ext(fname, newext);
```

|          |                                                                           |                           |
|----------|---------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                      | Description               |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file to use.          |
| newext   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new extension to use. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ext = filename_change_ext(file_find_first(working_directory + "*.*", 0), "");
```

The above code gets the name of the file (as a string) with the
extension part removed.
