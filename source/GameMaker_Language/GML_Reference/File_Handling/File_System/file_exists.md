# file_exists

This function will return true if the specified file exists and false if
it does not. Note that the function can only be used to check *local*
files, but not any files stored on a remote server.

#### Syntax:

``` gml
file_exists(fname);
```

|          |                                                                           |                                    |
|----------|---------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                      | Description                        |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if file_exists("level.txt")
{
    file = file_text_open_read("level.txt");
}
```

This would check for a file and if it exists it is opened for reading.
