# filename_name

Using this function returns the name part of the indicated file, *with*
the extension but *without* the path.

#### Syntax:

``` gml
filename_name(fname);
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
name = filename_name(file_find_first("C:/Games/*.doc", 0));
```

The above code gets the name (as a string) of the first "doc" type file
found in the specified directory.
