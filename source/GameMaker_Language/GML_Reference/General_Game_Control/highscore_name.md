# highscore_name

With this function you can retrieve the name string that has been stored
in the high score list at the given position. If no name has been
entered, the string "Unknown" will be returned.

#### Syntax:

``` gml
highscore_name(place);
```

|          |                                                                      |                                |
|----------|----------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                 | Description                    |
| place    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The place on the table (1-10). |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var i = 9;
repeat(10)
{
    name[i] = highscore_name(i + 1);
    i -= 1;
}
```

The above code will loop through the high score list and store all the
names in an array.
