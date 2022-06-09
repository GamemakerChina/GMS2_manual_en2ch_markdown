# random

This function is good for probabilities where returning an integer
(whole number) is not necessary. For example, random(100) will return a
value from 0 to 99, but that value can be 22.56473! You can also use
real numbers and not integers in this function like this - random(0.5) ,
which will return a value between 0 and 0.4999999. **NOTE** : This
function will return the same value every time the game is run afresh
due to the fact that GameMaker generates the same initial random seed
every time to make debugging code a far easier task. To avoid this
behaviour use [ randomise() ](randomise) at the start of your game.

#### Syntax:

``` gml
random(n);
```

|          |                                                                         |                                                                |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                    |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The upper range from which the random number will be selected. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (random(10) &amp;gt;= 9)
{
    score += 100;
}
```

This will produce approximately a one in ten chance of adding 100 to the
score.
