# darcsin

Returns the inverse sine of x, in that if dsin(x)=n , darcsin(n)=x , and
the resulting number will be between -90 and 90. **NOTE** : This will
only accept a number between -1 and 1 (anything else will throw an
error). **NOTE** : This function returns a value in degrees, not
radians.

#### Syntax:

``` gml
darcsin(x);
```

|          |                                                                         |                                          |
|----------|-------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                    | Description                              |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to return the inverse sine of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = darcsin(-1);
```

This will set "val" to -90.
