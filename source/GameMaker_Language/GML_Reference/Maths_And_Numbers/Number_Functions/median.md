# median

This function returns the median of the input values, that is, the
middle value. When the number of arguments is even, the smaller of the
two middle values is returned and the function can have as many
arguments as required (note that more arguments will mean that the
function will be slower to parse) which must all be real values. This
means that, for example, median(43, 12, 25, 19, 6) would return 19 as it
is the middle value between all the rest.

#### Syntax:

``` gml
median(val1, val2, ... max_val);
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
x = median( 0, x, room_width ); y = median( 0, y, room_height );
```

This will stop the player from exiting any side of the room, by using
median as a clamp. If the player, for instance, moves to the left of the
room boundary, its x will be smaller than 0. This will mean the middle
number of the first of the medians will be 0, so the player will be
jumped to (0,y).
