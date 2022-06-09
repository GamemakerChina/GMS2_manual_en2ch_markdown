# ini_key_delete

With this function you can remove the selected key (and its
corresponding value) from an ini file.

#### Syntax:

``` gml
ini_key_delete(section, key);
```

|          |                                                                           |                                   |
|----------|---------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                      | Description                       |
| section  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The section to delete a key from. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The key to delete.                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ini_open("savedata.ini"); ini_write_real("save1","Score",score);
 ini_key_delete("save1","Score");
 ini_close();
```

This example will open "savedata.ini" and write a value to "save1" \>
"Score". It will then delete the "Score" key and close the .ini file.
