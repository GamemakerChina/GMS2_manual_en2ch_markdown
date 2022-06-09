# highscore_value

With this function you can retrieve the score value that has been stored
in the high score list at the given position. If no score has been
entered, the function will return 0.

#### Syntax:

``` gml
highscore_value(place);
```

|          |                                                                      |                                |
|----------|----------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                 | Description                    |
| place    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The place on the table (1-10). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var i = 9;
repeat(10)
{
    scr[i] = highscore_value(i + 1);
    i -= 1;
}
```

The above code will loop through the high score list and store all the
scores in an array.
