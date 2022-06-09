# file_text_eoln

With this function you can get GameMaker to check the currently opened
file to see if the line being read has finished. The function returns
true if the end of the line has been reached and false otherwise.

#### Syntax:

``` gml
file_text_eoln(fileid);
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
var file = file_text_open_read(working_directory + "Game_Data.txt");
var num = 0; while (!file_text_eoln(file))
{
    score_array[num] = file_text_read_real(file);
    num++;
}
file_text_close(file);
```

The above code opens a file for reading then reads the values from a
single line into an array.
