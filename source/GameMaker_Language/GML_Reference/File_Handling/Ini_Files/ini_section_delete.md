# ini_section_delete

With this function you can delete a whole section of an ini file, which
will also remove all key-value pairs that are associated with it.

#### Syntax:

``` gml
ini_section_delete(section);
```

|          |                                                                           |                        |
|----------|---------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                      | Description            |
| section  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The section to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ini_open("savedata.ini"); ini_write_real("save1", "Score", score ); ini_section_delete("save1");
 ini_close();
```

This example will open "savedata.ini" and write a value to "save1" \>
"Score". It will then delete the "save1" section and close the .ini
file.
