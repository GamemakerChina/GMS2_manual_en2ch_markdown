# random_range

This function returns a random number between the specified range, and
this return value does not need to be an integer. For example,
random_range(20,50) will return a random number from 20 to 50, but the
value may be a real number like 38.65265. Real numbers can also be used
as input arguments. **NOTE** : This function will return the same value
every time the game is run afresh due to the fact that GameMaker
generates the same initial random seed every time to make debugging code
a far easier task. To avoid this behaviour use [ randomise()
](randomise) at the start of your game.

#### Syntax:

``` gml
random_range(n1, n2);
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
score += random_range(500, 600);
```

This will add anywhere between 500 and 600, to the total score.
