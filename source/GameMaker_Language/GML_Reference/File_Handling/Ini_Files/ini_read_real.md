# ini_read_real

You can use this function to read a number from an ini data file. Ini
Files are split into **sections** and then each section is subsequently
split into **key** - **value** pairs. So a typical ini file would look
something like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Files/IniExample.png)  

#### Syntax:

``` gml
ini_read_real(section, key, default);
```

|          |                                                                           |                                                                                                                            |
|----------|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                                                                                |
| section  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The section of the .ini to read from.                                                                                      |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The key within the relevant section of the .ini to read from.                                                              |
| default  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The value to return if a value is not found in the defined place (or the .ini file does not exist). Must be a real number. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
ini_open("savedata.ini"); score = ini_read_real("save1", "score", 0 ); ini_close();
```

This will open "savedata.ini" and set score to the value under "save1"
\> "score" in it, then close the .ini again. Should there be no value
under "save1" \> "score", or there no "savedata.ini" file present, score
will be set to 0.
