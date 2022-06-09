# power

This will return the value of a number multiplied by itself "n" number
of times. For example, power(5,3) will multiply 5 by itself 3 times and
return 125, which is the same as saying 5\*5\*5=125. Please note that
the "x" value (the number to change) *cannot* be a negative value.

#### Syntax:

``` gml
power(x, n);
```

|          |                                                                         |                                         |
|----------|-------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                    | Description                             |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to change.                   |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | How many times to multiply x by itself. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
score += power(dmg, 3);
```

This will add the value of held in the variable "dmg" to the power of 3
to the score variable.
