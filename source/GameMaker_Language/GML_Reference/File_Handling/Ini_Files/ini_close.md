# ini_close

This function should be called the moment you are finished reading or
writing to any open ini file. If you do not use the function after you
have used any of the ini write functions, then nothing will be written
to disk, as the file information is held in memory until this function
is called, which forces the write. If you try to open an ini without
having previously closed another one (or the same one) you will get an
error too. The function will also return a string with the ini file
encoded into it. This string can then be saved to a server and/or used
again along with the function [ ini_open_from_string()
](ini_open_from_string) to re-create the ini.

#### Syntax:

``` gml
ini_close();
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("savedata.ini");
score = ini_read_real("save1", "score", 0);
ini_close();
```

This will open "savedata.ini" and read a value from the section "save1"
with the key "score", then close the ini file. If there is no value
under "save1" called "score" or there is no "savedata.ini" file present,
0 will be returned and a new ini file created.
