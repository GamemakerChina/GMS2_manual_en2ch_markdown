# file_text_writeln

With this function you can write a new line to an opened text file. In
this way you can skip lines or write information on a line by line basis
(see example code below).

#### Syntax:

``` gml
file_text_writeln(fileid);
```

|          |                                                                                                                    |                             |
|----------|--------------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                               | Description                 |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to edit. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var file = file_text_open_write(working_directory + "hiscore.txt");
for (var i = 0; i &amp;lt; 10; ++i;)
{
    file_text_write_real(file, scr[i]);
    file_text_writeln(file);
    file_text_write_string(file, scr_name[i]);
    file_text_writeln(file);
}
file_text_close(file);
```

The above code opens a file for writing and then loops through two
arrays, writing each array value to a new line of the file. The file is
then closed when the loop has finished.
