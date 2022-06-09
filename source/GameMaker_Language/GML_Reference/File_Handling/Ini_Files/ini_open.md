# ini_open

This opens an ini_file for reading and/writing. If the ini_file does not
exist at the location you are checking, GameMaker may create one, but
only if you write data to it. If you have only read information from the
ini file, then the default values for the read function will be
returned, but the ini file will *not* actually be created. Please note
that you can only have **one** ini file open at any one time and
remember to use [ ini_close() ](ini_close) once you're finished
reading/writing from the .ini file as the information is not actually
stored to disk until then (it is also stored in memory until the file is
closed). **WARNING!** This function may not work as you expect due to
GameMaker being sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
ini_open(name);
```

|          |                                                                           |                                 |
|----------|---------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                      | Description                     |
| name     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The filename for the .ini file. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ini_open("Settings/savedata.ini"); score = ini_read_real("save1", "score", 0); ini_close();
```

This will open 'savedata.ini' and read the score value under the section
"save1" with the key "score" in it, then close the .ini again. Should
there be no value under "save1", "score" or there is no "savedata.ini"
file present, score will be set to 0 (the default value). Note that the
ini file has been placed in the sub-directory "Settings", which is the
folder that holds the ini file in the Asset Browser included files.
