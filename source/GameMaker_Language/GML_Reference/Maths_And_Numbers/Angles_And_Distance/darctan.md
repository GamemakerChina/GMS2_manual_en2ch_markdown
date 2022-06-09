# darctan

Returns the inverse tangent of x. This will accept any number as, unlike
[ dtan() ](dtan) , darctan() asymptotes are on the y axis so it just
means you'll never get returned a number greater than 90 or less than
-90. **NOTE** : This function returns a value in degrees, not radians.

#### Syntax:

``` gml
darctan(x);
```

|          |                                                                         |                                             |
|----------|-------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                    | Description                                 |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to return the inverse tangent of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = darctan(1);
```

This will set "val" to -45.
