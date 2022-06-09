# max

This function returns the maximum of the input values, of which it can
have up to 16. For example max(12, 96, 32, 75) will return 96 as that is
the highest of all the input values.

#### Syntax:

``` gml
max(val1, val2, ... max_val);
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
x = max(x, 0);
```

This will stop the player from exiting the left of the room. This works
by constantly setting its x to either itself or 0, whichever is larger.
If the player exits the left, its x would be smaller than 0 (ie
negative), so it'll get set straight back.
