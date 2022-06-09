# irandom_range

This function is similar to [ random_range() ](random_range) only
with integer values as the input. You supply the low value for the range
as well as the high value, and the function will return a random integer
value within (and including) the given range. For example,
irandom_range(10, 35) will return an integer between 10 and 35
*inclusive* . As with the [ irandom() ](irandom) function, real
numbers can be used, in which case they will be rounded down to the
nearest integer EG: irandom_range(6.2,9.9) will give a value between 6
and 9. ** NOTE ** This function will return the same value every time
the game is run afresh due to the fact that GameMaker: Studio generates
the same initial random seed every time to make debugging code a far
easier task. To avoid this behaviour use [ randomise() ](randomise)
at the start of your game.

#### Syntax:

``` gml
irandom_range(n1, n2);
```

|          |                                                                         |                                                                          |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                              |
| n1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The low end of the range from which the random number will be selected.  |
| n2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The high end of the range from which the random number will be selected. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
score += irandom_range(500, 600);
```

This will add an integer value anywhere between 500 and 600 (inclusive)
to the total score.
