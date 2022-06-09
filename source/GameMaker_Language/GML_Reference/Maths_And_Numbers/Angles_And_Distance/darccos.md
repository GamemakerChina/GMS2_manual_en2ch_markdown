# darccos

Returns the inverse cosine of x, in that if dcos(val)=n , darccos(n)=val
, and the resulting number will be between 180 and 0. **NOTE** : This
will only accept a number between -1 and 1 (anything else will throw an
error). **NOTE** : This function returns a value in degrees, not
radians.

#### Syntax:

``` gml
darccos(val)
```

|          |                                                                         |                                            |
|----------|-------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                    | Description                                |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to return the inverse cosine of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = arccos(-1);
```

This will set "val" to 180.
