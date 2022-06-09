# arcsin

Returns the inverse sine of x, in that if sin(x)=n , arcsin(n)=x , and
the resulting number will be between -pi/2 and pi/2. **NOTE** : This
will only accept a value between -1 and 1 (anything else will throw an
error). **NOTE** : This function returns a value in radians, not
degrees.

#### Syntax:

``` gml
arcsin(x);
```

|          |                                                                         |                                          |
|----------|-------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                    | Description                              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to return the inverse sine of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = arcsin(0);
```

This will set val to 0.
