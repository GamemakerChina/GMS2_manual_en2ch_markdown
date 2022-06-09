# frac

This function returns the fractional part of n, that is, the part behind
the decimal dot. It will return *only* the decimals behind the dot of a
value, so frac(3.125) will return 0.125, frac(6.921) will return 0.921,
etc...

#### Syntax:

``` gml
frac(n);
```

|          |                                                                         |                       |
|----------|-------------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                    | Description           |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to change. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = frac(3.4);
```

This will set val to 0.4.
