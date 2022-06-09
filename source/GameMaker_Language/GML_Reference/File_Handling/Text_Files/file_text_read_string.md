# file_text_read_string

With this function you can read a string from a text file and the
function returns that value to be used or stored in a variable.

#### Syntax:

``` gml
file_text_read_string(fileid);
```

|          |                                                                                                                    |                                  |
|----------|--------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                               | Description                      |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to read from. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var file = file_text_open_read(working_directory + "hiscore.txt");
for (var i = 0; i &amp;lt; 10; ++i;)
{
    scr[i] = file_text_read_real(file);
    file_text_readln(file);
    scr_name[i] = file_text_read_string(file);
    file_text_readln(file);
}
file_text_close(file);
```

The above code opens a file for reading and then loops through the lines
of the file reading alternately a real number value and a string into
two different arrays for future use. The file is then closed when the
loop has finished.
