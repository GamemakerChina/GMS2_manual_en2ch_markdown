# logn

This function is similar to the [ log2(n) ](log2) and
[log10(n)](log10) functions, only you stipulate the log base value.
For example, logn(5,25) will return how many 5's we need to multiply to
get 25 (which is 2).

#### Syntax:

``` gml
logn(n, val);
```

|          |                                                                         |                  |
|----------|-------------------------------------------------------------------------|------------------|
| Argument | Type                                                                    | Description      |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The log base.    |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The input value. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
logval = logn(5, num);
```

The above code gets the log5 of the value stored in "num".
