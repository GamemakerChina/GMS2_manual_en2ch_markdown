# sqrt

If you multiply a number with itself, you get the square of that number,
but sometimes you want to do the reverse and get the square root of a
number. So to find what number has been multiplied with itself to get
any given *positive* value we use this function. For example: sqrt(9)
will return 3 since 3\*3=9.

#### Syntax:

``` gml
sqrt(val);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to get the square root of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
num = sqrt(exp);
```

The above code will set the variable "num" to hold the square root of
the value contained in "exp".
