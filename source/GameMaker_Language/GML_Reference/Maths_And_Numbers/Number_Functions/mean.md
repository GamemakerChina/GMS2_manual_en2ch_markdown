# mean

This function works by adding up all the input values and then dividing
them by their own number. You can have as many arguments as you require
(note that more arguments will mean that the function will be slower to
parse). So, mean(2, 6, 9, 32) returns 12.25 as 2+6+9+32=49 and
49/4=12.25.

#### Syntax:

``` gml
mean(val1, val2, ... max_val);
```

|                  |                                                                         |                        |
|------------------|-------------------------------------------------------------------------|------------------------|
| Argument         | Type                                                                    | Description            |
| val0 ... max_val |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The values to compare. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
xmiddle = mean(obj_player1.x, obj_player2.x, obj_player3.x); ymiddle = mean(obj_player1.y, obj_player2.y, obj_player3.y);
```

This will set xmiddle and ymiddle to the x and y coordinates of the
average of the coordinates of three player objects, obj_player1,
obj_player2 and obj_player3. You could, for instance, use this to keep
the game camera focused on all three players instead of just one.
