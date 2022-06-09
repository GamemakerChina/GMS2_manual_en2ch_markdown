# dtan

In a right angled triangle *dtan(val) = Opposite / Adjacent* where "val"
is one of the three angles. **NOTE** : A vast number of values (90, or
-90 for example) will error with this function due to their returning
infinity, a graph representation of this would produce asymptotes at
these values. **NOTE** : This function takes a value in degrees not
radians

#### Syntax:

``` gml
dtan(val);
```

|          |                                                                         |                                                  |
|----------|-------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                    | Description                                      |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle (in degrees) to return the tangent of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = dtan(45);
```

This will set "val" to 1.
