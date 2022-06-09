# file_text_close

Once you have finished working with a given file (whether reading from
it or writing to it), you must close the file again, or else you risk
losing the information contained within. This also prevents memory leaks
and makes sure that you never go over the file limit by having more than
32 files open.

#### Syntax:

``` gml
file_text_close(fileid);
```

|          |                                                                                                                    |                              |
|----------|--------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                               | Description                  |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to close. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var file = file_text_open_write(working_directory + "Game_Data.txt");
while (!file_text_eof(file))
{
    file_text_readln(file);
}
file_text_write_string(file, level_data);
file_text_close(file);
```

The above code opens a file for writing then loops through the lines of
text already written to the file until it reaches the end. At this point
it writes a string and then closes the file again.
