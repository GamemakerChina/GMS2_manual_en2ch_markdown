# file_text_write_string

With this function you can write a string to a previously opened text
file. If the file already contains information, this information will be
erased and the string will be written at the beginning of the file,
unless you have opened the file with the [ file_text_open_append()
](file_text_open_append) . You can also avoid this by using the [
file_text_readln() ](file_text_readln) function along with the [
file_text_eof() ](file_text_eof) function to loop through the
contents of the file until you get to the end and then start writing.

#### Syntax:

``` gml
file_text_write_string(fileid, str);
```

|          |                                                                                                                    |                                  |
|----------|--------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                               | Description                      |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to edit.      |
| str      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | The string to write to the file. |

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
