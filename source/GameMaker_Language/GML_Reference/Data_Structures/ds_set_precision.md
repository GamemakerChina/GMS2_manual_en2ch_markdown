# ds_set_precision

When comparing values, for example when searching in a map or sorting a
list, GameMaker must decide when two values are equal. For strings and
integer values this is clear but for real numbers, due to floating point
round-off errors, seemingly equal numbers can easily become unequal. For
example, it's possible that **(5 / 3) \* 3** will *not* be equal to 5!
To help avoid this, a precision value is used on all real number
functions, and when the *difference between two numbers is smaller* than
this precision they are considered equal. The default a precision of
0.0000001 is used for all data structure functions unless changed by
this function. **NOTE** : This precision is used in all data structures
but not in other comparisons in GML!

#### Syntax:

``` gml
ds_set_precision(prec);
```

|          |                                                                      |                                         |
|----------|----------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                 | Description                             |
| prec     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The precision value (default 0.0000001) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_set_precision(0.0001);
```

The above code will change the default precision setting for all data
structure functions.
