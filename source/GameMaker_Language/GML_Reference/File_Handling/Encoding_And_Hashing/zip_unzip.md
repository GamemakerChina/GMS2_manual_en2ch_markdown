# zip_unzip

This function will open a stored zip file and extract its contents to
the given directory. Note that if you do not supply a full path to the
ZIP directory then the current drive *root* will be used, and if you
want to place it in a relative path to the game bundle working directory
then you should use the [ working_directory
](../File_Directories/working_directory) variable as part of the
path (relative paths using "." or ".." will not work as expected so
should be avoided). Note too that the zip must be either part of the
game bundle (ie: an [Included
File](../../../../Settings/Included_Files) ) or have been downloaded
to the storage area using
[http_get_file()](../../Asynchronous_Functions/HTTP/http_get_file) .
The function will return a value indicating the number of files
extracted, or it will return 0 or less if the extraction has failed.

#### Syntax:

``` gml
zip_unzip(zip_file, target_directory)
```

|                  |                                                                           |                                              |
|------------------|---------------------------------------------------------------------------|----------------------------------------------|
| Argument         | Type                                                                      | Description                                  |
| zip_file         |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The zip file to open                         |
| target_directory |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The target directory to extract the files to |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var num = zip_unzip("/downloads/level_data.zip", working_directory + "extracted/");
if num &amp;lt;= 0
{
    show_debug_message("Extraction Failed!");
}
```

The above code will open the zip file stored in the directory
"downloads" and extract its contents to the directory "extracted"
(creating that directory if it doesn't already exist) and then check to
see that the extraction has been correct, showing a debug message should
it fail.
