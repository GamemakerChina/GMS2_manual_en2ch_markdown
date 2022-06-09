# file_text_write_real

With this function you can write a number to the previously opened text
file. Note that as the value to be written can be a real number, all
decimals will be written with a "." point as separator. If the file
already contains information, this information will be erased and the
string will be written at the beginning of the file, unless you have
opened the file with the [ file_text_open_append()
](file_text_open_append) . You can also avoid this by using the [
file_text_readln() ](file_text_readln) function along with the [
file_text_eof() ](file_text_eof) function to loop through the
contents of the file until you get to the end and then start writing. It
is important to note that when writing very large numbers to a text file
using this function, it may be translated into a standard simplified
format, like "6.6624e+003", which cannot be read back in to GameMaker
correctly. To prevent issues like this, you should instead convert the
value to a string and use the function [ file_text_write_string()
](file_text_write_string) instead.

#### Syntax:

``` gml
file_text_write_real(fileid, val);
```

|          |                                                                                                                    |                                      |
|----------|--------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                               | Description                          |
| fileid   |  [Text File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Text_Files/file_text_open_read)  | The id of the file to edit.          |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                             | The real value to write to the file. |

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
