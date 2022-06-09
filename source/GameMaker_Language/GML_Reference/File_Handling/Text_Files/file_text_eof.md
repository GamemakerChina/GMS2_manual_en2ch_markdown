# file_text_eof

This function returns true when the end of a given opened text file has
been reached or false if not.

#### Syntax:

``` gml
file_text_eof(fileid);
```

|          |                                                                                                                    |                              |
|----------|--------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                               | Description                  |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var num = 0;
var file = file_text_open_read(working_directory + "Game_Data.txt");
while (!file_text_eof(file))
{
    str[num++] = file_text_readln(file);
}
file_text_close(file);
```

The above code opens a file for writing then loops through the lines of
text already written to the file until it reaches the end, storing each
line in the array "str".
